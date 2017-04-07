# api documentation for  [api-benchmark (v0.4.2)](http://www.api-benchmark.com/)  [![npm package](https://img.shields.io/npm/v/npmdoc-api-benchmark.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-api-benchmark) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-api-benchmark.svg)](https://travis-ci.org/npmdoc/node-npmdoc-api-benchmark)
#### A simple nodejs tool to measure and compare performances of api services

[![NPM](https://nodei.co/npm/api-benchmark.png?downloads=true)](https://www.npmjs.com/package/api-benchmark)

[![apidoc](https://npmdoc.github.io/node-npmdoc-api-benchmark/build/screenCapture.buildNpmdoc.browser.%2Fhome%2Ftravis%2Fbuild%2Fnpmdoc%2Fnode-npmdoc-api-benchmark%2Ftmp%2Fbuild%2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-api-benchmark/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-api-benchmark/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-api-benchmark/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Matteo Figus",
        "email": "matteofigus@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/matteofigus/api-benchmark/issues"
    },
    "contributors": [
        {
            "name": "Michael Sanford",
            "email": "michaelsanford0@gmail.com"
        },
        {
            "name": "Derek Myers",
            "email": "arcticpro@gmail.com"
        }
    ],
    "dependencies": {
        "give-me": "0.1.0",
        "superagent": "2.0.0",
        "underscore": "1.8.3"
    },
    "description": "A simple nodejs tool to measure and compare performances of api services",
    "devDependencies": {
        "http-test-servers": "1.0.0",
        "injectr": "^0.5.1",
        "jshint": "^2.9.2",
        "mocha": "2.5.3",
        "should": "8.4.0"
    },
    "directories": {},
    "dist": {
        "shasum": "15598bb5e8d534372a7dccdd8ac4a525b4518076",
        "tarball": "https://registry.npmjs.org/api-benchmark/-/api-benchmark-0.4.2.tgz"
    },
    "engines": {
        "node": ">=0.8.x",
        "npm": ">=1.2.x"
    },
    "gitHead": "fbbc05308bad75a27c06f4c8e8407a963b828a00",
    "homepage": "http://www.api-benchmark.com/",
    "keywords": [
        "benchmark",
        "api",
        "performance",
        "test",
        "load balancer",
        "deployment",
        "continuous delivery"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "matteofigus",
            "email": "matteofigus@gmail.com"
        }
    ],
    "name": "api-benchmark",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/matteofigus/api-benchmark.git"
    },
    "scripts": {
        "pretest": "jshint lib test templates index.js",
        "test": "node test/index"
    },
    "version": "0.4.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module api-benchmark](#apidoc.module.api-benchmark)
1.  [function <span class="apidocSignatureSpan">api-benchmark.</span>compare (services, endpoints, options, callback)](#apidoc.element.api-benchmark.compare)
1.  [function <span class="apidocSignatureSpan">api-benchmark.</span>getHtml (input, options, callback)](#apidoc.element.api-benchmark.getHtml)
1.  [function <span class="apidocSignatureSpan">api-benchmark.</span>measure (services, endpoints, options, callback)](#apidoc.element.api-benchmark.measure)
1.  object <span class="apidocSignatureSpan">api-benchmark.</span>benchmark_utils
1.  object <span class="apidocSignatureSpan">api-benchmark.</span>html_converter
1.  object <span class="apidocSignatureSpan">api-benchmark.</span>request_handler
1.  object <span class="apidocSignatureSpan">api-benchmark.</span>sanitise
1.  object <span class="apidocSignatureSpan">api-benchmark.</span>validator

#### [module api-benchmark.benchmark_utils](#apidoc.module.api-benchmark.benchmark_utils)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>cycleMessage (benchmark)](#apidoc.element.api-benchmark.benchmark_utils.cycleMessage)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getAverage (benchmarks)](#apidoc.element.api-benchmark.benchmark_utils.getAverage)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getBenchmarkAverage (benchmark, benchmarkName)](#apidoc.element.api-benchmark.benchmark_utils.getBenchmarkAverage)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getBenchmarksAverage (benchmarks)](#apidoc.element.api-benchmark.benchmark_utils.getBenchmarksAverage)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getDeviation (variance)](#apidoc.element.api-benchmark.benchmark_utils.getDeviation)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getFieldAverage (benchmarks, propertyName)](#apidoc.element.api-benchmark.benchmark_utils.getFieldAverage)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getHz (singleMean)](#apidoc.element.api-benchmark.benchmark_utils.getHz)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getMean (samples)](#apidoc.element.api-benchmark.benchmark_utils.getMean)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getMoe (samples, sem)](#apidoc.element.api-benchmark.benchmark_utils.getMoe)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getPercentile (samples, ptile)](#apidoc.element.api-benchmark.benchmark_utils.getPercentile)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getRelevantFields (benchmark)](#apidoc.element.api-benchmark.benchmark_utils.getRelevantFields)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getRme (moe, mean)](#apidoc.element.api-benchmark.benchmark_utils.getRme)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getSem (samples, deviation)](#apidoc.element.api-benchmark.benchmark_utils.getSem)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getSingleMean (mean, concurrencyLevel)](#apidoc.element.api-benchmark.benchmark_utils.getSingleMean)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getStats (benchmarks)](#apidoc.element.api-benchmark.benchmark_utils.getStats)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getSuccessful (benchmarks)](#apidoc.element.api-benchmark.benchmark_utils.getSuccessful)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getVariance (samples, mean)](#apidoc.element.api-benchmark.benchmark_utils.getVariance)
1.  [function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>sort (benchmarks)](#apidoc.element.api-benchmark.benchmark_utils.sort)

#### [module api-benchmark.html_converter](#apidoc.module.api-benchmark.html_converter)
1.  [function <span class="apidocSignatureSpan">api-benchmark.html_converter.</span>getHtml (input, options, callback)](#apidoc.element.api-benchmark.html_converter.getHtml)

#### [module api-benchmark.request_handler](#apidoc.module.api-benchmark.request_handler)
1.  [function <span class="apidocSignatureSpan">api-benchmark.request_handler.</span>make (req, suite, suiteName, requestAgent, callback)](#apidoc.element.api-benchmark.request_handler.make)
1.  [function <span class="apidocSignatureSpan">api-benchmark.request_handler.</span>setup (suiteName, suiteHref, suite, requestAgent)](#apidoc.element.api-benchmark.request_handler.setup)

#### [module api-benchmark.sanitise](#apidoc.module.api-benchmark.sanitise)
1.  [function <span class="apidocSignatureSpan">api-benchmark.sanitise.</span>endpoint (endpointName, endpoint)](#apidoc.element.api-benchmark.sanitise.endpoint)
1.  [function <span class="apidocSignatureSpan">api-benchmark.sanitise.</span>initialInput (services, endpoints, options, callback)](#apidoc.element.api-benchmark.sanitise.initialInput)
1.  [function <span class="apidocSignatureSpan">api-benchmark.sanitise.</span>options (options)](#apidoc.element.api-benchmark.sanitise.options)

#### [module api-benchmark.validator](#apidoc.module.api-benchmark.validator)
1.  [function <span class="apidocSignatureSpan">api-benchmark.validator.</span>checkCallback (callback)](#apidoc.element.api-benchmark.validator.checkCallback)
1.  [function <span class="apidocSignatureSpan">api-benchmark.validator.</span>checkEndpoints (endpoints)](#apidoc.element.api-benchmark.validator.checkEndpoints)
1.  [function <span class="apidocSignatureSpan">api-benchmark.validator.</span>checkServices (services)](#apidoc.element.api-benchmark.validator.checkServices)



# <a name="apidoc.module.api-benchmark"></a>[module api-benchmark](#apidoc.module.api-benchmark)

#### <a name="apidoc.element.api-benchmark.compare"></a>[function <span class="apidocSignatureSpan">api-benchmark.</span>compare (services, endpoints, options, callback)](#apidoc.element.api-benchmark.compare)
- description and source-code
```javascript
compare = function (services, endpoints, options, callback){

  var parameters = sanitise.initialInput(services, endpoints, options, callback),
      suites = new SuitesManager(superagent, new DebugHelper());

  suites.setOptions(parameters.options)
        .addEndpoints(parameters.endpoints)
        .addServices(parameters.services)
        .onBenchResults(parameters.callback)
        .start();

  return suites;
}
```
- example usage
```shell
...
var services = {
  server1: "http://myserver:myport/mypath/",
  server2: "http://myserver2:myport2/mypath2/",
};

var routes = { route1: 'route1', route2: 'route2' };

apiBenchmark.compare(services, routes, function(err, results){
  console.log(results);
  // displays some stats, including the winner!
});
'''

All the Http verbs and headers are supported.
...
```

#### <a name="apidoc.element.api-benchmark.getHtml"></a>[function <span class="apidocSignatureSpan">api-benchmark.</span>getHtml (input, options, callback)](#apidoc.element.api-benchmark.getHtml)
- description and source-code
```javascript
getHtml = function (input, options, callback){

  if(_.isFunction(options)){
    callback = options;
    options = {};
  }

  fs.readFile(path.join(__dirname, '../templates/report.html'), 'utf-8', function(err, template){

    if(err) {
      return callback(err);
			}

    var obj = {
      benchmark: input,
      info: {
        date: new Date(),
        apiName: _.keys(input)[0]
      }
    };

    var templateWithData = template.replace('{{ data }}', JSON.stringify(obj).replace(/<\/script>/g, '</scr"+"ipt>'));

    callback(null, templateWithData);
  });
}
```
- example usage
```shell
...
var service = {
  server1: "http://myserver:myport/mypath/"
};

var routes = { route1: 'route1', route2: 'route2' };

apiBenchmark.measure(service, routes, function(err, results){
  apiBenchmark.getHtml(results, function(error, html){
    console.log(html);
    // now save it yourself to a file and enjoy
  });
});
'''

### Route object
...
```

#### <a name="apidoc.element.api-benchmark.measure"></a>[function <span class="apidocSignatureSpan">api-benchmark.</span>measure (services, endpoints, options, callback)](#apidoc.element.api-benchmark.measure)
- description and source-code
```javascript
measure = function (services, endpoints, options, callback){

  var parameters = sanitise.initialInput(services, endpoints, options, callback),
      suites = new SuitesManager(superagent, new DebugHelper());

  suites.setOptions(parameters.options)
        .addEndpoints(parameters.endpoints)
        .addServices(parameters.services)
        .onBenchResults(parameters.callback)
        .start();

  return suites;
}
```
- example usage
```shell
...

var service = {
  server1: "http://myserver:myport/mypath/"
};

var routes = { route1: 'route1', route2: 'route2' };

apiBenchmark.measure(service, routes, function(err, results){
  console.log(results);
  // displays some stats!
});
'''

### compare(services, [routes](#route-object), [[options](#options-object), ] callback)
...
```



# <a name="apidoc.module.api-benchmark.benchmark_utils"></a>[module api-benchmark.benchmark_utils](#apidoc.module.api-benchmark.benchmark_utils)

#### <a name="apidoc.element.api-benchmark.benchmark_utils.cycleMessage"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>cycleMessage (benchmark)](#apidoc.element.api-benchmark.benchmark_utils.cycleMessage)
- description and source-code
```javascript
cycleMessage = function (benchmark) {

  var formatNumber = function(number) {
    number = String(number).split('.');
    return number[0].replace(/(?=(?:\d{3})+$)(?!\b)/g, ',') + (number[1] ? '.' + number[1] : '');
  };

  var hz = benchmark.hz,
      stats = benchmark.stats,
      size = stats.sample.length,
      pm = '\xb1';

  return format(settings.successMessages.CYCLE_MESSAGE,
                benchmark.name,
                formatNumber(hz.toFixed(hz < 100 ? 2 : 0)),
                pm + stats.rme.toFixed(2),
                size,
                (size === 1 ? '' : 's'));
}
```
- example usage
```shell
...
    result.errors[settings.errorCodes.MAX_SINGLE_MEAN_EXCEEDED]=[];
			}

  result.errors[settings.errorCodes.MAX_SINGLE_MEAN_EXCEEDED].push(maxSingleMeanErr);
}

this.results.push(result);
this.emit('cycle', benchmarkUtils.cycleMessage(result));
return step;
  };

  this.run = function(){
var self = this;

giveMe.sequence(_.map(this.steps, function(step){ return step.run; }), function(callbacks){
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getAverage"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getAverage (benchmarks)](#apidoc.element.api-benchmark.benchmark_utils.getAverage)
- description and source-code
```javascript
getAverage = function (benchmarks){
  return _.compose(benchmarkUtils.sort, benchmarkUtils.getSuccessful, benchmarkUtils.getBenchmarksAverage)(benchmarks);
}
```
- example usage
```shell
...
_.forEach(benchmarks, function(benchmark, k){
  if(this.results[this.serviceNames[k]]){
    this.results[this.serviceNames[k]][currentName] = benchmark;
  }
}, this);
    },
    get: function(){
var averages = benchmarkUtils.getAverage(this.results);

if(averages.length > 1){
  this.results[averages[0].name].isFastest = true;
  this.results[averages[averages.length - 1].name].isSlowest = true;
}

return this.results;
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getBenchmarkAverage"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getBenchmarkAverage (benchmark, benchmarkName)](#apidoc.element.api-benchmark.benchmark_utils.getBenchmarkAverage)
- description and source-code
```javascript
getBenchmarkAverage = function (benchmark, benchmarkName){
  var stats = benchmarkUtils.getStats(benchmark),
      av = benchmarkUtils.getFieldAverage;

  return {
    name: benchmarkName,
    stats: {
      moe: av(stats, 'moe'),
      rme: av(stats, 'rme'),
      deviation: av(stats, 'deviation'),
      variance: av(stats, 'variance'),
      mean: av(stats, 'mean'),
      sem: av(stats, 'sem'),
      p75: av(stats, 'p75'),
      p95: av(stats, 'p95'),
      p99: av(stats, 'p99'),
      p999: av(stats, 'p999')
    },
    hz: av(benchmark, 'hz')
  };
}
```
- example usage
```shell
...
      p999: av(stats, 'p999')
    },
    hz: av(benchmark, 'hz')
  };
},
getBenchmarksAverage: function(benchmarks){
  return  _.map(benchmarks, function(benchmark, benchmarkName){
    return benchmarkUtils.getBenchmarkAverage(benchmark, benchmarkName);
  });
},
getFieldAverage: function(benchmarks, propertyName){
  var valuesArray = _.pluck(benchmarks, propertyName);
  return _.reduce(valuesArray, function(memo, num){
    return memo + num;
  }, 0) / valuesArray.length;
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getBenchmarksAverage"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getBenchmarksAverage (benchmarks)](#apidoc.element.api-benchmark.benchmark_utils.getBenchmarksAverage)
- description and source-code
```javascript
getBenchmarksAverage = function (benchmarks){
  return  _.map(benchmarks, function(benchmark, benchmarkName){
    return benchmarkUtils.getBenchmarkAverage(benchmark, benchmarkName);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getDeviation"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getDeviation (variance)](#apidoc.element.api-benchmark.benchmark_utils.getDeviation)
- description and source-code
```javascript
getDeviation = function (variance){
  return Math.sqrt(variance);
}
```
- example usage
```shell
...
  response: benchmark.response
};

stats.mean = __.getMean(benchmark.stats.sample);
stats.singleMean = __.getSingleMean(stats.mean, benchmark.options.concurrencyLevel);
result.hz = __.getHz(stats.singleMean);
stats.variance = __.getVariance(benchmark.stats.sample, stats.mean);
stats.deviation = __.getDeviation(stats.variance);
stats.sem = __.getSem(benchmark.stats.sample, stats.deviation);
stats.moe = __.getMoe(benchmark.stats.sample, stats.sem);
stats.rme = __.getRme(stats.moe, stats.mean);
stats.p75 = __.getPercentile(benchmark.stats.sample, 0.75);
stats.p95 = __.getPercentile(benchmark.stats.sample, 0.95);
stats.p99 = __.getPercentile(benchmark.stats.sample, 0.99);
stats.p999 = __.getPercentile(benchmark.stats.sample, 0.999);
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getFieldAverage"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getFieldAverage (benchmarks, propertyName)](#apidoc.element.api-benchmark.benchmark_utils.getFieldAverage)
- description and source-code
```javascript
getFieldAverage = function (benchmarks, propertyName){
  var valuesArray = _.pluck(benchmarks, propertyName);
  return _.reduce(valuesArray, function(memo, num){
    return memo + num;
  }, 0) / valuesArray.length;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getHz"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getHz (singleMean)](#apidoc.element.api-benchmark.benchmark_utils.getHz)
- description and source-code
```javascript
getHz = function (singleMean){
  return 1/singleMean;
}
```
- example usage
```shell
...
  options: benchmark.options,
  request: benchmark.request,
  response: benchmark.response
};

stats.mean = __.getMean(benchmark.stats.sample);
stats.singleMean = __.getSingleMean(stats.mean, benchmark.options.concurrencyLevel);
result.hz = __.getHz(stats.singleMean);
stats.variance = __.getVariance(benchmark.stats.sample, stats.mean);
stats.deviation = __.getDeviation(stats.variance);
stats.sem = __.getSem(benchmark.stats.sample, stats.deviation);
stats.moe = __.getMoe(benchmark.stats.sample, stats.sem);
stats.rme = __.getRme(stats.moe, stats.mean);
stats.p75 = __.getPercentile(benchmark.stats.sample, 0.75);
stats.p95 = __.getPercentile(benchmark.stats.sample, 0.95);
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getMean"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getMean (samples)](#apidoc.element.api-benchmark.benchmark_utils.getMean)
- description and source-code
```javascript
getMean = function (samples){
  return _.reduce(samples, function(memo, num){
    return memo + num;
  }, 0) / samples.length;
}
```
- example usage
```shell
...
  },
  errors: benchmark.errors,
  options: benchmark.options,
  request: benchmark.request,
  response: benchmark.response
};

stats.mean = __.getMean(benchmark.stats.sample);
stats.singleMean = __.getSingleMean(stats.mean, benchmark.options.concurrencyLevel);
result.hz = __.getHz(stats.singleMean);
stats.variance = __.getVariance(benchmark.stats.sample, stats.mean);
stats.deviation = __.getDeviation(stats.variance);
stats.sem = __.getSem(benchmark.stats.sample, stats.deviation);
stats.moe = __.getMoe(benchmark.stats.sample, stats.sem);
stats.rme = __.getRme(stats.moe, stats.mean);
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getMoe"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getMoe (samples, sem)](#apidoc.element.api-benchmark.benchmark_utils.getMoe)
- description and source-code
```javascript
getMoe = function (samples, sem){
<span class="apidocCodeCommentSpan">  /**
   * T-Distribution two-tailed critical values for 95% confidence
   * http://www.itl.nist.gov/div898/handbook/eda/section3/eda3672.htm
   */
</span>  var tTable = {
    '1':  12.706,'2':  4.303, '3':  3.182, '4':  2.776, '5':  2.571, '6':  2.447,
    '7':  2.365, '8':  2.306, '9':  2.262, '10': 2.228, '11': 2.201, '12': 2.179,
    '13': 2.16,  '14': 2.145, '15': 2.131, '16': 2.12,  '17': 2.11,  '18': 2.101,
    '19': 2.093, '20': 2.086, '21': 2.08,  '22': 2.074, '23': 2.069, '24': 2.064,
    '25': 2.06,  '26': 2.056, '27': 2.052, '28': 2.048, '29': 2.045, '30': 2.042,
    'infinity': 1.96
  };

  var critical = tTable[Math.round(samples.length - 1) || 1] || tTable.infinity;
  return sem * critical;
}
```
- example usage
```shell
...

stats.mean = __.getMean(benchmark.stats.sample);
stats.singleMean = __.getSingleMean(stats.mean, benchmark.options.concurrencyLevel);
result.hz = __.getHz(stats.singleMean);
stats.variance = __.getVariance(benchmark.stats.sample, stats.mean);
stats.deviation = __.getDeviation(stats.variance);
stats.sem = __.getSem(benchmark.stats.sample, stats.deviation);
stats.moe = __.getMoe(benchmark.stats.sample, stats.sem);
stats.rme = __.getRme(stats.moe, stats.mean);
stats.p75 = __.getPercentile(benchmark.stats.sample, 0.75);
stats.p95 = __.getPercentile(benchmark.stats.sample, 0.95);
stats.p99 = __.getPercentile(benchmark.stats.sample, 0.99);
stats.p999 = __.getPercentile(benchmark.stats.sample, 0.999);

result.stats = _.extend(result.stats, stats);
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getPercentile"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getPercentile (samples, ptile)](#apidoc.element.api-benchmark.benchmark_utils.getPercentile)
- description and source-code
```javascript
getPercentile = function (samples, ptile){
  var values = _.clone(samples).sort(function (a, b) { return a - b; }),
      pos = ptile * (values.length + 1);

  if (pos < 1) {
    return values[0];
  } else if (pos >= values.length) {
    return values[values.length - 1];
  } else {
    var lower = values[Math.floor(pos) - 1];
    var upper = values[Math.ceil(pos) - 1];

    return lower + (pos - Math.floor(pos)) * (upper - lower);
  }
}
```
- example usage
```shell
...
stats.singleMean = __.getSingleMean(stats.mean, benchmark.options.concurrencyLevel);
result.hz = __.getHz(stats.singleMean);
stats.variance = __.getVariance(benchmark.stats.sample, stats.mean);
stats.deviation = __.getDeviation(stats.variance);
stats.sem = __.getSem(benchmark.stats.sample, stats.deviation);
stats.moe = __.getMoe(benchmark.stats.sample, stats.sem);
stats.rme = __.getRme(stats.moe, stats.mean);
stats.p75 = __.getPercentile(benchmark.stats.sample, 0.75);
stats.p95 = __.getPercentile(benchmark.stats.sample, 0.95);
stats.p99 = __.getPercentile(benchmark.stats.sample, 0.99);
stats.p999 = __.getPercentile(benchmark.stats.sample, 0.999);

result.stats = _.extend(result.stats, stats);

return result;
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getRelevantFields"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getRelevantFields (benchmark)](#apidoc.element.api-benchmark.benchmark_utils.getRelevantFields)
- description and source-code
```javascript
getRelevantFields = function (benchmark){

  var __ = benchmarkUtils,
      stats = {};

  var result = {
    name: benchmark.name,
    href: benchmark.href,
    stats: {
      sample: benchmark.stats.sample
    },
    errors: benchmark.errors,
    options: benchmark.options,
    request: benchmark.request,
    response: benchmark.response
  };

  stats.mean = __.getMean(benchmark.stats.sample);
  stats.singleMean = __.getSingleMean(stats.mean, benchmark.options.concurrencyLevel);
  result.hz = __.getHz(stats.singleMean);
  stats.variance = __.getVariance(benchmark.stats.sample, stats.mean);
  stats.deviation = __.getDeviation(stats.variance);
  stats.sem = __.getSem(benchmark.stats.sample, stats.deviation);
  stats.moe = __.getMoe(benchmark.stats.sample, stats.sem);
  stats.rme = __.getRme(stats.moe, stats.mean);
  stats.p75 = __.getPercentile(benchmark.stats.sample, 0.75);
  stats.p95 = __.getPercentile(benchmark.stats.sample, 0.95);
  stats.p99 = __.getPercentile(benchmark.stats.sample, 0.99);
  stats.p999 = __.getPercentile(benchmark.stats.sample, 0.999);

  result.stats = _.extend(result.stats, stats);

  return result;
}
```
- example usage
```shell
...
  };

  this.addResult = function(step){
step.stats.sample = _.filter(step.stats.sample, function(item){
  return _.isNumber(item);
});

var result = benchmarkUtils.getRelevantFields(_.pick(step, 'name', 'href', 'stats', 'errors', 'options', 'request', 'response')),
				maxMeanErr,
				maxSingleMeanErr;

if(!!step.options.maxMean && (result.stats.mean > step.options.maxMean)){
  maxMeanErr = {
    code: settings.errorCodes.MAX_MEAN_EXCEEDED,
    details: step.name,
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getRme"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getRme (moe, mean)](#apidoc.element.api-benchmark.benchmark_utils.getRme)
- description and source-code
```javascript
getRme = function (moe, mean){
  return (moe / mean) * 100 || 0;
}
```
- example usage
```shell
...
stats.mean = __.getMean(benchmark.stats.sample);
stats.singleMean = __.getSingleMean(stats.mean, benchmark.options.concurrencyLevel);
result.hz = __.getHz(stats.singleMean);
stats.variance = __.getVariance(benchmark.stats.sample, stats.mean);
stats.deviation = __.getDeviation(stats.variance);
stats.sem = __.getSem(benchmark.stats.sample, stats.deviation);
stats.moe = __.getMoe(benchmark.stats.sample, stats.sem);
stats.rme = __.getRme(stats.moe, stats.mean);
stats.p75 = __.getPercentile(benchmark.stats.sample, 0.75);
stats.p95 = __.getPercentile(benchmark.stats.sample, 0.95);
stats.p99 = __.getPercentile(benchmark.stats.sample, 0.99);
stats.p999 = __.getPercentile(benchmark.stats.sample, 0.999);

result.stats = _.extend(result.stats, stats);
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getSem"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getSem (samples, deviation)](#apidoc.element.api-benchmark.benchmark_utils.getSem)
- description and source-code
```javascript
getSem = function (samples, deviation){
  return deviation / Math.sqrt(samples.length);
}
```
- example usage
```shell
...
};

stats.mean = __.getMean(benchmark.stats.sample);
stats.singleMean = __.getSingleMean(stats.mean, benchmark.options.concurrencyLevel);
result.hz = __.getHz(stats.singleMean);
stats.variance = __.getVariance(benchmark.stats.sample, stats.mean);
stats.deviation = __.getDeviation(stats.variance);
stats.sem = __.getSem(benchmark.stats.sample, stats.deviation);
stats.moe = __.getMoe(benchmark.stats.sample, stats.sem);
stats.rme = __.getRme(stats.moe, stats.mean);
stats.p75 = __.getPercentile(benchmark.stats.sample, 0.75);
stats.p95 = __.getPercentile(benchmark.stats.sample, 0.95);
stats.p99 = __.getPercentile(benchmark.stats.sample, 0.99);
stats.p999 = __.getPercentile(benchmark.stats.sample, 0.999);
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getSingleMean"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getSingleMean (mean, concurrencyLevel)](#apidoc.element.api-benchmark.benchmark_utils.getSingleMean)
- description and source-code
```javascript
getSingleMean = function (mean, concurrencyLevel){
  // Mean across all concurrent requests.
  // Should represent the mean for each single request in a multi-concurrent context.

  return mean/concurrencyLevel;
}
```
- example usage
```shell
...
  errors: benchmark.errors,
  options: benchmark.options,
  request: benchmark.request,
  response: benchmark.response
};

stats.mean = __.getMean(benchmark.stats.sample);
stats.singleMean = __.getSingleMean(stats.mean, benchmark.options.concurrencyLevel);
result.hz = __.getHz(stats.singleMean);
stats.variance = __.getVariance(benchmark.stats.sample, stats.mean);
stats.deviation = __.getDeviation(stats.variance);
stats.sem = __.getSem(benchmark.stats.sample, stats.deviation);
stats.moe = __.getMoe(benchmark.stats.sample, stats.sem);
stats.rme = __.getRme(stats.moe, stats.mean);
stats.p75 = __.getPercentile(benchmark.stats.sample, 0.75);
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getStats"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getStats (benchmarks)](#apidoc.element.api-benchmark.benchmark_utils.getStats)
- description and source-code
```javascript
getStats = function (benchmarks){
  return _.map(benchmarks, function(benchmark){
    return benchmark.stats;
  });
}
```
- example usage
```shell
...
var _ = require('underscore');

var benchmarkUtils = {
  getAverage: function(benchmarks){
return _.compose(benchmarkUtils.sort, benchmarkUtils.getSuccessful, benchmarkUtils.getBenchmarksAverage)(benchmarks);
  },
  getBenchmarkAverage: function(benchmark, benchmarkName){
var stats = benchmarkUtils.getStats(benchmark),
    av = benchmarkUtils.getFieldAverage;

return {
  name: benchmarkName,
  stats: {
    moe: av(stats, 'moe'),
    rme: av(stats, 'rme'),
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getSuccessful"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getSuccessful (benchmarks)](#apidoc.element.api-benchmark.benchmark_utils.getSuccessful)
- description and source-code
```javascript
getSuccessful = function (benchmarks){
  return _.filter(benchmarks, function(benchmark){
    return isFinite(benchmark.hz);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.getVariance"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>getVariance (samples, mean)](#apidoc.element.api-benchmark.benchmark_utils.getVariance)
- description and source-code
```javascript
getVariance = function (samples, mean){
  return _.reduce(samples, function(sum, x) {
    return sum + Math.pow(x - mean, 2);
  }, 0) / (samples.length - 1) || 0;
}
```
- example usage
```shell
...
  request: benchmark.request,
  response: benchmark.response
};

stats.mean = __.getMean(benchmark.stats.sample);
stats.singleMean = __.getSingleMean(stats.mean, benchmark.options.concurrencyLevel);
result.hz = __.getHz(stats.singleMean);
stats.variance = __.getVariance(benchmark.stats.sample, stats.mean);
stats.deviation = __.getDeviation(stats.variance);
stats.sem = __.getSem(benchmark.stats.sample, stats.deviation);
stats.moe = __.getMoe(benchmark.stats.sample, stats.sem);
stats.rme = __.getRme(stats.moe, stats.mean);
stats.p75 = __.getPercentile(benchmark.stats.sample, 0.75);
stats.p95 = __.getPercentile(benchmark.stats.sample, 0.95);
stats.p99 = __.getPercentile(benchmark.stats.sample, 0.99);
...
```

#### <a name="apidoc.element.api-benchmark.benchmark_utils.sort"></a>[function <span class="apidocSignatureSpan">api-benchmark.benchmark_utils.</span>sort (benchmarks)](#apidoc.element.api-benchmark.benchmark_utils.sort)
- description and source-code
```javascript
sort = function (benchmarks){
  return _.sortBy(benchmarks, function(benchmark){
    return benchmark.stats.mean + benchmark.stats.moe;
  });
}
```
- example usage
```shell
...
  'infinity': 1.96
};

var critical = tTable[Math.round(samples.length - 1) || 1] || tTable.infinity;
return sem * critical;
  },
  getPercentile: function(samples, ptile){
var values = _.clone(samples).sort(function (a, b) { return a - b; }),
    pos = ptile * (values.length + 1);

if (pos < 1) {
  return values[0];
} else if (pos >= values.length) {
  return values[values.length - 1];
} else {
...
```



# <a name="apidoc.module.api-benchmark.html_converter"></a>[module api-benchmark.html_converter](#apidoc.module.api-benchmark.html_converter)

#### <a name="apidoc.element.api-benchmark.html_converter.getHtml"></a>[function <span class="apidocSignatureSpan">api-benchmark.html_converter.</span>getHtml (input, options, callback)](#apidoc.element.api-benchmark.html_converter.getHtml)
- description and source-code
```javascript
getHtml = function (input, options, callback){

  if(_.isFunction(options)){
    callback = options;
    options = {};
  }

  fs.readFile(path.join(__dirname, '../templates/report.html'), 'utf-8', function(err, template){

    if(err) {
      return callback(err);
			}

    var obj = {
      benchmark: input,
      info: {
        date: new Date(),
        apiName: _.keys(input)[0]
      }
    };

    var templateWithData = template.replace('{{ data }}', JSON.stringify(obj).replace(/<\/script>/g, '</scr"+"ipt>'));

    callback(null, templateWithData);
  });
}
```
- example usage
```shell
...
var service = {
  server1: "http://myserver:myport/mypath/"
};

var routes = { route1: 'route1', route2: 'route2' };

apiBenchmark.measure(service, routes, function(err, results){
  apiBenchmark.getHtml(results, function(error, html){
    console.log(html);
    // now save it yourself to a file and enjoy
  });
});
'''

### Route object
...
```



# <a name="apidoc.module.api-benchmark.request_handler"></a>[module api-benchmark.request_handler](#apidoc.module.api-benchmark.request_handler)

#### <a name="apidoc.element.api-benchmark.request_handler.make"></a>[function <span class="apidocSignatureSpan">api-benchmark.request_handler.</span>make (req, suite, suiteName, requestAgent, callback)](#apidoc.element.api-benchmark.request_handler.make)
- description and source-code
```javascript
make = function (req, suite, suiteName, requestAgent, callback){
  requestAgent.make(req, function(err, response){

    var res = !!response ? {
      header: response.header,
      statusCode: response.statusCode,
      body: response.text,
      type: response.type
    } : false;

    if(err && !res){
      var code = err.code || 'Unknown';

      return callback({
        code: code,
        message: err.message || code
      }, res);
    }
    else if(!!suite.endpoint.expectedStatusCode && suite.endpoint.expectedStatusCode !== response.status) {
      return callback({
        code: settings.errorCodes.HTTP_STATUS_CODE_NOT_MATCHING,
        message: format(settings.errorMessages.HTTP_STATUS_CODE_NOT_MATCHING, suite.endpoint.expectedStatusCode, response.status
, suiteName)
      }, res);
			}
    else {
				callback(null, res);
			}
  });
}
```
- example usage
```shell
...

var format = require('./format');
var settings = require('./settings');
var _ = require('underscore');

module.exports = {
  make: function(req, suite, suiteName, requestAgent, callback){
    requestAgent.make(req, function(err, response){

var res = !!response ? {
  header: response.header,
  statusCode: response.statusCode,
  body: response.text,
  type: response.type
} : false;
...
```

#### <a name="apidoc.element.api-benchmark.request_handler.setup"></a>[function <span class="apidocSignatureSpan">api-benchmark.request_handler.</span>setup (suiteName, suiteHref, suite, requestAgent)](#apidoc.element.api-benchmark.request_handler.setup)
- description and source-code
```javascript
setup = function (suiteName, suiteHref, suite, requestAgent){
  var self = this,
      req = _.extend(_.clone(suite.endpoint), { url: suiteHref }),
      suiteOptions = {
        expectedStatusCode: suite.endpoint.expectedStatusCode,
        maxMean: suite.endpoint.maxMean,
        maxSingleMean: suite.endpoint.maxSingleMean,
        method: suite.endpoint.method
      },
      suiteRequest = {};

  if(!!suite.endpoint.headers){
    suiteRequest.headers = _.isFunction(suite.endpoint.headers) ? 'Dynamic headers' : suite.endpoint.headers;
		}

  if(!!suite.endpoint.data){
    suiteRequest.data = _.isFunction(suite.endpoint.data) ? 'Dynamic data' : suite.endpoint.data;
		}

  if(!!suite.endpoint.query){
    suiteRequest.query = _.isFunction(suite.endpoint.query) ? 'Dynamic query' : suite.endpoint.query;
  }

  suite.runner.add(suiteName, suiteHref, suiteOptions, suiteRequest, function(done){
    self.make(req, suite, suiteName, requestAgent, done);
  });
}
```
- example usage
```shell
...
  _.forEach(this.services, function(service, serviceName){
    _.forEach(this.routes, function(route){

      var routeHref = url.resolve(service, route.endpoint.route),
          routeName = serviceName + '/' + route.name,
          self = this;

      requestHandler.setup(routeName, routeHref, route, self.requestAgent);
    }, this);
  }, this);

  return this;
},
handleErrors: function(route){
  var self = this;
...
```



# <a name="apidoc.module.api-benchmark.sanitise"></a>[module api-benchmark.sanitise](#apidoc.module.api-benchmark.sanitise)

#### <a name="apidoc.element.api-benchmark.sanitise.endpoint"></a>[function <span class="apidocSignatureSpan">api-benchmark.sanitise.</span>endpoint (endpointName, endpoint)](#apidoc.element.api-benchmark.sanitise.endpoint)
- description and source-code
```javascript
endpoint = function (endpointName, endpoint){
  var output = _.clone(endpoint);

  if(_.isString(output)) {
    output = { route: output };
		}

  output.method = output.method || 'get';

  return output;
}
```
- example usage
```shell
...
  if(!this.validate(validator.checkEndpoints, endpoints)) {
    return this;
			}

  _.forEach(endpoints, function(endpoint, endpointName){
    this.routes.push({
      name: endpointName,
      endpoint: sanitise.endpoint(endpointName, endpoint),
      runner: new Runner(this.options)
    });
  }, this);

  return this;
},
addServices: function(services){
...
```

#### <a name="apidoc.element.api-benchmark.sanitise.initialInput"></a>[function <span class="apidocSignatureSpan">api-benchmark.sanitise.</span>initialInput (services, endpoints, options, callback)](#apidoc.element.api-benchmark.sanitise.initialInput)
- description and source-code
```javascript
initialInput = function (services, endpoints, options, callback){
  var output = _.clone({
    services: services,
    endpoints: endpoints,
    options: options,
    callback: callback
  });

  if(_.isFunction(options)){
    output.callback = options;
    output.options = {};
  }

  return output;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.api-benchmark.sanitise.options"></a>[function <span class="apidocSignatureSpan">api-benchmark.sanitise.</span>options (options)](#apidoc.element.api-benchmark.sanitise.options)
- description and source-code
```javascript
options = function (options){
  var output = options || {};

 return _.extend(output, {
    delay: output.delay || 0,
    debug: output.debug || false,
    maxTime: output.maxTime || 10,
    minSamples: output.minSamples || 20,
    maxConcurrentRequests: output.maxConcurrentRequests || 100,
    runMode: output.runMode || 'sequence',
    stopOnError: output.stopOnError !== undefined ? output.stopOnError : true
  });
}
```
- example usage
```shell
...
runNext: function(){
  if(!!this.routes && (this.routes.length) > 0 && !!this.routes[this.current]){
    this.routes[this.current].runner.run();
    this.current++;
  }
},
setOptions: function(options){
  this.options = sanitise.options(options);

  if(!this.options.debug) {
    debugHelper.shutUp();
			}

  return this;
},
...
```



# <a name="apidoc.module.api-benchmark.validator"></a>[module api-benchmark.validator](#apidoc.module.api-benchmark.validator)

#### <a name="apidoc.element.api-benchmark.validator.checkCallback"></a>[function <span class="apidocSignatureSpan">api-benchmark.validator.</span>checkCallback (callback)](#apidoc.element.api-benchmark.validator.checkCallback)
- description and source-code
```javascript
checkCallback = function (callback){
  if(!callback || !_.isFunction(callback)){
    throw new Error(settings.errorMessages.VALIDATION_CALLBACK);
		}

  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.api-benchmark.validator.checkEndpoints"></a>[function <span class="apidocSignatureSpan">api-benchmark.validator.</span>checkEndpoints (endpoints)](#apidoc.element.api-benchmark.validator.checkEndpoints)
- description and source-code
```javascript
checkEndpoints = function (endpoints){
  if(!endpoints || !_.isObject(endpoints) || _.isArray(endpoints) || _.keys(endpoints).length < 1) {
    return (settings.errorMessages.VALIDATION_ENDPOINTS);
		}

  var methods = _.map(endpoints, function(endpoint){
    return _.isString(endpoint) ? 'get' : (endpoint.method || 'get');
  });

  if(_.without(methods, 'get', 'post', 'put', 'head', 'patch', 'delete', 'trace', 'options').length > 0) {
    return (settings.errorMessages.VALIDATION_ENDPOINT_VERB);
		}

  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.api-benchmark.validator.checkServices"></a>[function <span class="apidocSignatureSpan">api-benchmark.validator.</span>checkServices (services)](#apidoc.element.api-benchmark.validator.checkServices)
- description and source-code
```javascript
checkServices = function (services){
  if(!services || !_.isObject(services) || _.isArray(services) || _.keys(services).length < 1) {
    return (settings.errorMessages.VALIDATION_SERVICES);
		}

  return true;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
