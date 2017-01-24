#!/usr/bin/env node

var download = require('download-git-repo')
var program = require('commander')
var exists = require('fs').existsSync
var os = require('os')
var path = require('path')
var rm = require('rimraf').sync
var uid = require('uid')
var ora = require('ora')
var chalk = require('chalk')
var inquirer = require('inquirer')

/**
 * Usage.
 */
program
    .usage('[project-name]')
    .option('-c, --clone', 'use git clone')

program.parse(process.argv);
/**
 * Download a generate from a template repo.
 *
 * @param {String} template
 */
// console.log(program)
var template = program.args[0]
var tmp = __dirname + "\\" + template
var spinner = ora('downloading template')
download("github:chuanshuoye/vue-project-frame", tmp, function(err) {
    if (err) console.log('Failed to download repo ' + template + ': ' + err.message.trim())
})
