<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [bitburner](./bitburner.md) &gt; [NS](./bitburner.ns.md) &gt; [spawn](./bitburner.ns.spawn.md)

## NS.spawn() method

Terminate current script and start another in 10 seconds.

**Signature:**

```typescript
spawn(script: string, numThreads?: number, ...args: (string | number | boolean)[]): void;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  script | string | Filename of script to execute. |
|  numThreads | number | _(Optional)_ Integer number of threads for new script. Defaults to 1. |
|  args | (string \| number \| boolean)\[\] | Additional arguments to pass into the new script that is being run. |

**Returns:**

void

## Remarks

RAM cost: 2 GB

Terminates the current script, and then after a delay of about 10 seconds it will execute the newly-specified script. The purpose of this function is to execute a new script without being constrained by the RAM usage of the current one. This function can only be used to run scripts on the local server.

Because this function immediately terminates the script, it does not have a return value.

Running this function with a numThreads argument of 0 or less will cause a runtime error.

## Example


```js
//The following example will execute the script ‘foo.js’ with 10 threads and the arguments ‘foodnstuff’ and 90:
ns.spawn('foo.js', 10, 'foodnstuff', 90);
```

