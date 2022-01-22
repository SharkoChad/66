npm WARN deprecated snekfetch@3.6.4: use node-fetch instead
npm WARN deprecated discord.js@11.6.4: no longer supported

added 6 packages, removed 756 packages, changed 2 packages, and audited 260 packages in 19s

22 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
 npm install -g npm@8.3.2
npm ERR! code EACCES
npm ERR! syscall rename
npm ERR! path /nix/store/bwxril521b35zlf4x2g32hll64rzfhck-nodejs-16.7.0/lib/node_modules/npm
npm ERR! dest /nix/store/bwxril521b35zlf4x2g32hll64rzfhck-nodejs-16.7.0/lib/node_modules/.npm-29iRSGy0
npm ERR! errno -13
npm ERR! Error: EACCES: permission denied, rename '/nix/store/bwxril521b35zlf4x2g32hll64rzfhck-nodejs-16.7.0/lib/node_modules/npm' -> '/nix/store/bwxril521b35zlf4x2g32hll64rzfhck-nodejs-16.7.0/lib/node_modules/.npm-29iRSGy0'
 npm install --legacy-peer-deps && npm start

removed 1 package, and audited 259 packages in 2s

22 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

> qbot@7.3.0 start
> ts-node src/main.ts

/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750
    return new TSError(diagnosticText, diagnosticCodes);
           ^
TSError: ⨯ Unable to compile TypeScript:
src/structures/QbotClient.ts:17:13 - error TS2345: Argument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.
  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.

 17             intents: [
                ~~~~~~~~~~
 18                 'GUILDS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~
... 
 21                 'GUILD_MESSAGE_REACTIONS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 22             ]
    ~~~~~~~~~~~~~
src/structures/QbotClient.ts:28:21 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

28             if(this.application.botPublic) return console.log(securityText);
                       ~~~~~~~~~~~
src/structures/QbotClient.ts:36:21 - error TS2322: Type '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.
  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.

36                     type: config.activity.type,
                       ~~~~

  node_modules/discord.js/typings/index.d.ts:276:69
    276   public setActivity(name: string | null, options?: { url?: string, type?: ActivityType | number }): Promise<Presence>;
                                                                            ~~~~
    The expected type comes from property 'type' which is declared here on type '{ url?: string; type?: number | ActivityType; }'
src/structures/QbotClient.ts:66:31 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

66                 discordClient.application.commands.set(slashCommands);
                                 ~~~~~~~~~~~

    at createTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750:12)
    at reportTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:754:19)
    at getOutput (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:941:36)
    at Object.compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1243:30)
    at Module.m._compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1370:30)
    at Module._extensions..js (node:internal/modules/cjs/loader:1153:10)
    at Object.require.extensions.<computed> [as .ts] (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1374:12)
    at Module.load (node:internal/modules/cjs/loader:981:32)
    at Function.Module._load (node:internal/modules/cjs/loader:822:12)
    at Module.require (node:internal/modules/cjs/loader:1005:19) {
  diagnosticText: "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m17\x1B[0m:\x1B[93m13\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2345: \x1B[0mArgument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.\n" +
    "  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.\n" +
    '\n' +
    '\x1B[7m 17\x1B[0m             intents: [\n' +
    '\x1B[7m   \x1B[0m \x1B[91m            ~~~~~~~~~~\x1B[0m\n' +
    "\x1B[7m 18\x1B[0m                 'GUILDS',\n" +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~~~~~~~~~~~~~\x1B[0m\n' +
    '\x1B[7m...\x1B[0m \n' +
    "\x1B[7m 21\x1B[0m                 'GUILD_MESSAGE_REACTIONS',\n" +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~\x1B[0m\n' +
    '\x1B[7m 22\x1B[0m             ]\n' +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~\x1B[0m\n' +
    "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m28\x1B[0m:\x1B[93m21\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2339: \x1B[0mProperty 'application' does not exist on type 'QbotClient'.\n" +
    '\n' +
    '\x1B[7m28\x1B[0m             if(this.application.botPublic) return console.log(securityText);\n' +
    '\x1B[7m  \x1B[0m \x1B[91m                    ~~~~~~~~~~~\x1B[0m\n' +
    `\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m36\x1B[0m:\x1B[93m21\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2322: \x1B[0mType '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.\n` +
    `  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.\n` +
 npm install --legacy-peer-deps && npm start

up to date, audited 259 packages in 3s

22 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

> qbot@7.3.0 start
> ts-node src/main.ts

/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750
    return new TSError(diagnosticText, diagnosticCodes);
           ^
TSError: ⨯ Unable to compile TypeScript:
src/structures/QbotClient.ts:17:13 - error TS2345: Argument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.
  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.

 17             intents: [
                ~~~~~~~~~~
 18                 'GUILDS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~
... 
 21                 'GUILD_MESSAGE_REACTIONS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 22             ]
    ~~~~~~~~~~~~~
src/structures/QbotClient.ts:28:21 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

28             if(this.application.botPublic) return console.log(securityText);
                       ~~~~~~~~~~~
src/structures/QbotClient.ts:36:21 - error TS2322: Type '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.
  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.

36                     type: config.activity.type,
                       ~~~~

  node_modules/discord.js/typings/index.d.ts:276:69
    276   public setActivity(name: string | null, options?: { url?: string, type?: ActivityType | number }): Promise<Presence>;
                                                                            ~~~~
    The expected type comes from property 'type' which is declared here on type '{ url?: string; type?: number | ActivityType; }'
src/structures/QbotClient.ts:66:31 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

66                 discordClient.application.commands.set(slashCommands);
                                 ~~~~~~~~~~~

    at createTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750:12)
    at reportTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:754:19)
    at getOutput (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:941:36)
    at Object.compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1243:30)
    at Module.m._compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1370:30)
    at Module._extensions..js (node:internal/modules/cjs/loader:1153:10)
    at Object.require.extensions.<computed> [as .ts] (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1374:12)
    at Module.load (node:internal/modules/cjs/loader:981:32)
    at Function.Module._load (node:internal/modules/cjs/loader:822:12)
    at Module.require (node:internal/modules/cjs/loader:1005:19) {
  diagnosticText: "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m17\x1B[0m:\x1B[93m13\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2345: \x1B[0mArgument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.\n" +
    "  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.\n" +
    '\n' +
    '\x1B[7m 17\x1B[0m             intents: [\n' +
    '\x1B[7m   \x1B[0m \x1B[91m            ~~~~~~~~~~\x1B[0m\n' +
    "\x1B[7m 18\x1B[0m                 'GUILDS',\n" +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~~~~~~~~~~~~~\x1B[0m\n' +
    '\x1B[7m...\x1B[0m \n' +
    "\x1B[7m 21\x1B[0m                 'GUILD_MESSAGE_REACTIONS',\n" +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~\x1B[0m\n' +
    '\x1B[7m 22\x1B[0m             ]\n' +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~\x1B[0m\n' +
    "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m28\x1B[0m:\x1B[93m21\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2339: \x1B[0mProperty 'application' does not exist on type 'QbotClient'.\n" +
    '\n' +
    '\x1B[7m28\x1B[0m             if(this.application.botPublic) return console.log(securityText);\n' +
    '\x1B[7m  \x1B[0m \x1B[91m                    ~~~~~~~~~~~\x1B[0m\n' +
    `\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m36\x1B[0m:\x1B[93m21\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2322: \x1B[0mType '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.\n` +
    `  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.\n` +
 npm install --legacy-peer-deps && npm start

up to date, audited 259 packages in 2s

22 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

> qbot@7.3.0 start
> ts-node src/main.ts

/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750
    return new TSError(diagnosticText, diagnosticCodes);
           ^
TSError: ⨯ Unable to compile TypeScript:
src/structures/QbotClient.ts:17:13 - error TS2345: Argument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.
  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.

 17             intents: [
                ~~~~~~~~~~
 18                 'GUILDS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~
... 
 21                 'GUILD_MESSAGE_REACTIONS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 22             ]
    ~~~~~~~~~~~~~
src/structures/QbotClient.ts:28:21 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

28             if(this.application.botPublic) return console.log(securityText);
                       ~~~~~~~~~~~
src/structures/QbotClient.ts:36:21 - error TS2322: Type '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.
  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.

36                     type: config.activity.type,
                       ~~~~

  node_modules/discord.js/typings/index.d.ts:276:69
    276   public setActivity(name: string | null, options?: { url?: string, type?: ActivityType | number }): Promise<Presence>;
                                                                            ~~~~
    The expected type comes from property 'type' which is declared here on type '{ url?: string; type?: number | ActivityType; }'
src/structures/QbotClient.ts:66:31 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

66                 discordClient.application.commands.set(slashCommands);
                                 ~~~~~~~~~~~

    at createTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750:12)
    at reportTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:754:19)
    at getOutput (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:941:36)
    at Object.compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1243:30)
    at Module.m._compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1370:30)
    at Module._extensions..js (node:internal/modules/cjs/loader:1153:10)
    at Object.require.extensions.<computed> [as .ts] (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1374:12)
    at Module.load (node:internal/modules/cjs/loader:981:32)
    at Function.Module._load (node:internal/modules/cjs/loader:822:12)
    at Module.require (node:internal/modules/cjs/loader:1005:19) {
  diagnosticText: "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m17\x1B[0m:\x1B[93m13\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2345: \x1B[0mArgument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.\n" +
    "  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.\n" +
    '\n' +
    '\x1B[7m 17\x1B[0m             intents: [\n' +
    '\x1B[7m   \x1B[0m \x1B[91m            ~~~~~~~~~~\x1B[0m\n' +
    "\x1B[7m 18\x1B[0m                 'GUILDS',\n" +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~~~~~~~~~~~~~\x1B[0m\n' +
    '\x1B[7m...\x1B[0m \n' +
    "\x1B[7m 21\x1B[0m                 'GUILD_MESSAGE_REACTIONS',\n" +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~\x1B[0m\n' +
    '\x1B[7m 22\x1B[0m             ]\n' +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~\x1B[0m\n' +
    "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m28\x1B[0m:\x1B[93m21\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2339: \x1B[0mProperty 'application' does not exist on type 'QbotClient'.\n" +
    '\n' +
    '\x1B[7m28\x1B[0m             if(this.application.botPublic) return console.log(securityText);\n' +
    '\x1B[7m  \x1B[0m \x1B[91m                    ~~~~~~~~~~~\x1B[0m\n' +
    `\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m36\x1B[0m:\x1B[93m21\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2322: \x1B[0mType '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.\n` +
    `  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.\n` +
 npm install --legacy-peer-deps && npm start

up to date, audited 259 packages in 2s

22 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

> qbot@7.3.0 start
> ts-node src/main.ts

/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750
    return new TSError(diagnosticText, diagnosticCodes);
           ^
TSError: ⨯ Unable to compile TypeScript:
src/structures/QbotClient.ts:17:13 - error TS2345: Argument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.
  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.

 17             intents: [
                ~~~~~~~~~~
 18                 'GUILDS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~
... 
 21                 'GUILD_MESSAGE_REACTIONS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 22             ]
    ~~~~~~~~~~~~~
src/structures/QbotClient.ts:28:21 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

28             if(this.application.botPublic) return console.log(securityText);
                       ~~~~~~~~~~~
src/structures/QbotClient.ts:36:21 - error TS2322: Type '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.
  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.

36                     type: config.activity.type,
                       ~~~~

  node_modules/discord.js/typings/index.d.ts:276:69
    276   public setActivity(name: string | null, options?: { url?: string, type?: ActivityType | number }): Promise<Presence>;
                                                                            ~~~~
    The expected type comes from property 'type' which is declared here on type '{ url?: string; type?: number | ActivityType; }'
src/structures/QbotClient.ts:66:31 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

66                 discordClient.application.commands.set(slashCommands);
                                 ~~~~~~~~~~~

    at createTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750:12)
    at reportTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:754:19)
    at getOutput (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:941:36)
    at Object.compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1243:30)
    at Module.m._compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1370:30)
    at Module._extensions..js (node:internal/modules/cjs/loader:1153:10)
    at Object.require.extensions.<computed> [as .ts] (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1374:12)
    at Module.load (node:internal/modules/cjs/loader:981:32)
    at Function.Module._load (node:internal/modules/cjs/loader:822:12)
    at Module.require (node:internal/modules/cjs/loader:1005:19) {
  diagnosticText: "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m17\x1B[0m:\x1B[93m13\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2345: \x1B[0mArgument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.\n" +
    "  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.\n" +
    '\n' +
    '\x1B[7m 17\x1B[0m             intents: [\n' +
    '\x1B[7m   \x1B[0m \x1B[91m            ~~~~~~~~~~\x1B[0m\n' +
    "\x1B[7m 18\x1B[0m                 'GUILDS',\n" +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~~~~~~~~~~~~~\x1B[0m\n' +
    '\x1B[7m...\x1B[0m \n' +
    "\x1B[7m 21\x1B[0m                 'GUILD_MESSAGE_REACTIONS',\n" +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~\x1B[0m\n' +
    '\x1B[7m 22\x1B[0m             ]\n' +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~\x1B[0m\n' +
    "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m28\x1B[0m:\x1B[93m21\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2339: \x1B[0mProperty 'application' does not exist on type 'QbotClient'.\n" +
    '\n' +
    '\x1B[7m28\x1B[0m             if(this.application.botPublic) return console.log(securityText);\n' +
    '\x1B[7m  \x1B[0m \x1B[91m                    ~~~~~~~~~~~\x1B[0m\n' +
    `\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m36\x1B[0m:\x1B[93m21\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2322: \x1B[0mType '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.\n` +
    `  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.\n` +
 npm install --legacy-peer-deps && npm start

up to date, audited 259 packages in 2s

22 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

> qbot@7.3.0 start
> ts-node src/main.ts

/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750
    return new TSError(diagnosticText, diagnosticCodes);
           ^
TSError: ⨯ Unable to compile TypeScript:
src/structures/QbotClient.ts:17:13 - error TS2345: Argument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.
  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.

 17             intents: [
                ~~~~~~~~~~
 18                 'GUILDS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~
... 
 21                 'GUILD_MESSAGE_REACTIONS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 22             ]
    ~~~~~~~~~~~~~
src/structures/QbotClient.ts:28:21 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

28             if(this.application.botPublic) return console.log(securityText);
                       ~~~~~~~~~~~
src/structures/QbotClient.ts:36:21 - error TS2322: Type '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.
  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.

36                     type: config.activity.type,
                       ~~~~

  node_modules/discord.js/typings/index.d.ts:276:69
    276   public setActivity(name: string | null, options?: { url?: string, type?: ActivityType | number }): Promise<Presence>;
                                                                            ~~~~
    The expected type comes from property 'type' which is declared here on type '{ url?: string; type?: number | ActivityType; }'
src/structures/QbotClient.ts:66:31 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

66                 discordClient.application.commands.set(slashCommands);
                                 ~~~~~~~~~~~

    at createTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750:12)
    at reportTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:754:19)
    at getOutput (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:941:36)
    at Object.compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1243:30)
    at Module.m._compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1370:30)
    at Module._extensions..js (node:internal/modules/cjs/loader:1153:10)
    at Object.require.extensions.<computed> [as .ts] (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1374:12)
    at Module.load (node:internal/modules/cjs/loader:981:32)
    at Function.Module._load (node:internal/modules/cjs/loader:822:12)
    at Module.require (node:internal/modules/cjs/loader:1005:19) {
  diagnosticText: "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m17\x1B[0m:\x1B[93m13\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2345: \x1B[0mArgument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.\n" +
    "  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.\n" +
    '\n' +
    '\x1B[7m 17\x1B[0m             intents: [\n' +
    '\x1B[7m   \x1B[0m \x1B[91m            ~~~~~~~~~~\x1B[0m\n' +
    "\x1B[7m 18\x1B[0m                 'GUILDS',\n" +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~~~~~~~~~~~~~\x1B[0m\n' +
    '\x1B[7m...\x1B[0m \n' +
    "\x1B[7m 21\x1B[0m                 'GUILD_MESSAGE_REACTIONS',\n" +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~\x1B[0m\n' +
    '\x1B[7m 22\x1B[0m             ]\n' +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~\x1B[0m\n' +
    "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m28\x1B[0m:\x1B[93m21\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2339: \x1B[0mProperty 'application' does not exist on type 'QbotClient'.\n" +
    '\n' +
    '\x1B[7m28\x1B[0m             if(this.application.botPublic) return console.log(securityText);\n' +
    '\x1B[7m  \x1B[0m \x1B[91m                    ~~~~~~~~~~~\x1B[0m\n' +
    `\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m36\x1B[0m:\x1B[93m21\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2322: \x1B[0mType '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.\n` +
    `  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.\n` +
 npm install --legacy-peer-deps && npm start

up to date, audited 259 packages in 2s

22 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

> qbot@7.3.0 start
> ts-node src/main.ts

/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750
    return new TSError(diagnosticText, diagnosticCodes);
           ^
TSError: ⨯ Unable to compile TypeScript:
src/structures/QbotClient.ts:17:13 - error TS2345: Argument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.
  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.

 17             intents: [
                ~~~~~~~~~~
 18                 'GUILDS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~
... 
 21                 'GUILD_MESSAGE_REACTIONS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 22             ]
    ~~~~~~~~~~~~~
src/structures/QbotClient.ts:28:21 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

28             if(this.application.botPublic) return console.log(securityText);
                       ~~~~~~~~~~~
src/structures/QbotClient.ts:36:21 - error TS2322: Type '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.
  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.

36                     type: config.activity.type,
                       ~~~~

  node_modules/discord.js/typings/index.d.ts:276:69
    276   public setActivity(name: string | null, options?: { url?: string, type?: ActivityType | number }): Promise<Presence>;
                                                                            ~~~~
    The expected type comes from property 'type' which is declared here on type '{ url?: string; type?: number | ActivityType; }'
src/structures/QbotClient.ts:66:31 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

66                 discordClient.application.commands.set(slashCommands);
                                 ~~~~~~~~~~~

    at createTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750:12)
    at reportTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:754:19)
    at getOutput (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:941:36)
    at Object.compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1243:30)
    at Module.m._compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1370:30)
    at Module._extensions..js (node:internal/modules/cjs/loader:1153:10)
    at Object.require.extensions.<computed> [as .ts] (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1374:12)
    at Module.load (node:internal/modules/cjs/loader:981:32)
    at Function.Module._load (node:internal/modules/cjs/loader:822:12)
    at Module.require (node:internal/modules/cjs/loader:1005:19) {
  diagnosticText: "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m17\x1B[0m:\x1B[93m13\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2345: \x1B[0mArgument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.\n" +
 npm install --legacy-peer-deps && npm start

up to date, audited 259 packages in 2s

22 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

> qbot@7.3.0 start
> ts-node src/main.ts

/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750
    return new TSError(diagnosticText, diagnosticCodes);
           ^
TSError: ⨯ Unable to compile TypeScript:
src/structures/QbotClient.ts:17:13 - error TS2345: Argument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.
  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.

 17             intents: [
                ~~~~~~~~~~
 18                 'GUILDS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~
... 
 21                 'GUILD_MESSAGE_REACTIONS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 22             ]
    ~~~~~~~~~~~~~
src/structures/QbotClient.ts:28:21 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

28             if(this.application.botPublic) return console.log(securityText);
                       ~~~~~~~~~~~
src/structures/QbotClient.ts:36:21 - error TS2322: Type '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.
  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.

36                     type: config.activity.type,
                       ~~~~

  node_modules/discord.js/typings/index.d.ts:276:69
    276   public setActivity(name: string | null, options?: { url?: string, type?: ActivityType | number }): Promise<Presence>;
                                                                            ~~~~
    The expected type comes from property 'type' which is declared here on type '{ url?: string; type?: number | ActivityType; }'
src/structures/QbotClient.ts:66:31 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

66                 discordClient.application.commands.set(slashCommands);
                                 ~~~~~~~~~~~

    at createTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750:12)
    at reportTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:754:19)
    at getOutput (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:941:36)
    at Object.compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1243:30)
    at Module.m._compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1370:30)
    at Module._extensions..js (node:internal/modules/cjs/loader:1153:10)
    at Object.require.extensions.<computed> [as .ts] (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1374:12)
    at Module.load (node:internal/modules/cjs/loader:981:32)
    at Function.Module._load (node:internal/modules/cjs/loader:822:12)
    at Module.require (node:internal/modules/cjs/loader:1005:19) {
  diagnosticText: "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m17\x1B[0m:\x1B[93m13\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2345: \x1B[0mArgument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.\n" +
 npm install --legacy-peer-deps && npm start

up to date, audited 259 packages in 2s

22 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

> qbot@7.3.0 start
> ts-node src/main.ts

/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750
    return new TSError(diagnosticText, diagnosticCodes);
           ^
TSError: ⨯ Unable to compile TypeScript:
src/structures/QbotClient.ts:17:13 - error TS2345: Argument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.
  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.

 17             intents: [
                ~~~~~~~~~~
 18                 'GUILDS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~
... 
 21                 'GUILD_MESSAGE_REACTIONS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 22             ]
    ~~~~~~~~~~~~~
src/structures/QbotClient.ts:28:21 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

28             if(this.application.botPublic) return console.log(securityText);
                       ~~~~~~~~~~~
src/structures/QbotClient.ts:36:21 - error TS2322: Type '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.
  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.

36                     type: config.activity.type,
                       ~~~~

  node_modules/discord.js/typings/index.d.ts:276:69
    276   public setActivity(name: string | null, options?: { url?: string, type?: ActivityType | number }): Promise<Presence>;
                                                                            ~~~~
    The expected type comes from property 'type' which is declared here on type '{ url?: string; type?: number | ActivityType; }'
src/structures/QbotClient.ts:66:31 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

66                 discordClient.application.commands.set(slashCommands);
                                 ~~~~~~~~~~~

    at createTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750:12)
    at reportTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:754:19)
    at getOutput (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:941:36)
    at Object.compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1243:30)
    at Module.m._compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1370:30)
    at Module._extensions..js (node:internal/modules/cjs/loader:1153:10)
    at Object.require.extensions.<computed> [as .ts] (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1374:12)
    at Module.load (node:internal/modules/cjs/loader:981:32)
    at Function.Module._load (node:internal/modules/cjs/loader:822:12)
    at Module.require (node:internal/modules/cjs/loader:1005:19) {
  diagnosticText: "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m17\x1B[0m:\x1B[93m13\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2345: \x1B[0mArgument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.\n" +
 npm install --legacy-peer-deps && npm start

up to date, audited 259 packages in 2s

22 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

> qbot@7.3.0 start
> ts-node src/main.ts

/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750
    return new TSError(diagnosticText, diagnosticCodes);
           ^
TSError: ⨯ Unable to compile TypeScript:
src/structures/QbotClient.ts:17:13 - error TS2345: Argument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.
  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.

 17             intents: [
                ~~~~~~~~~~
 18                 'GUILDS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~
... 
 21                 'GUILD_MESSAGE_REACTIONS',
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 22             ]
    ~~~~~~~~~~~~~
src/structures/QbotClient.ts:28:21 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

28             if(this.application.botPublic) return console.log(securityText);
                       ~~~~~~~~~~~
src/structures/QbotClient.ts:36:21 - error TS2322: Type '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.
  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.

36                     type: config.activity.type,
                       ~~~~

  node_modules/discord.js/typings/index.d.ts:276:69
    276   public setActivity(name: string | null, options?: { url?: string, type?: ActivityType | number }): Promise<Presence>;
                                                                            ~~~~
    The expected type comes from property 'type' which is declared here on type '{ url?: string; type?: number | ActivityType; }'
src/structures/QbotClient.ts:66:31 - error TS2339: Property 'application' does not exist on type 'QbotClient'.

66                 discordClient.application.commands.set(slashCommands);
                                 ~~~~~~~~~~~

    at createTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:750:12)
    at reportTSError (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:754:19)
    at getOutput (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:941:36)
    at Object.compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1243:30)
    at Module.m._compile (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1370:30)
    at Module._extensions..js (node:internal/modules/cjs/loader:1153:10)
    at Object.require.extensions.<computed> [as .ts] (/home/runner/qbot-1/node_modules/ts-node/src/index.ts:1374:12)
    at Module.load (node:internal/modules/cjs/loader:981:32)
    at Function.Module._load (node:internal/modules/cjs/loader:822:12)
    at Module.require (node:internal/modules/cjs/loader:1005:19) {
  diagnosticText: "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m17\x1B[0m:\x1B[93m13\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2345: \x1B[0mArgument of type '{ intents: string[]; }' is not assignable to parameter of type 'ClientOptions'.\n" +
    "  Object literal may only specify known properties, and 'intents' does not exist in type 'ClientOptions'.\n" +
    '\n' +
    '\x1B[7m 17\x1B[0m             intents: [\n' +
    '\x1B[7m   \x1B[0m \x1B[91m            ~~~~~~~~~~\x1B[0m\n' +
    "\x1B[7m 18\x1B[0m                 'GUILDS',\n" +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~~~~~~~~~~~~~\x1B[0m\n' +
    '\x1B[7m...\x1B[0m \n' +
    "\x1B[7m 21\x1B[0m                 'GUILD_MESSAGE_REACTIONS',\n" +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~\x1B[0m\n' +
    '\x1B[7m 22\x1B[0m             ]\n' +
    '\x1B[7m   \x1B[0m \x1B[91m~~~~~~~~~~~~~\x1B[0m\n' +
    "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m28\x1B[0m:\x1B[93m21\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2339: \x1B[0mProperty 'application' does not exist on type 'QbotClient'.\n" +
    '\n' +
    '\x1B[7m28\x1B[0m             if(this.application.botPublic) return console.log(securityText);\n' +
    '\x1B[7m  \x1B[0m \x1B[91m                    ~~~~~~~~~~~\x1B[0m\n' +
    `\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m36\x1B[0m:\x1B[93m21\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2322: \x1B[0mType '"PLAYING" | "WATCHING" | "STREAMING" | "LISTENING" | "COMPETING"' is not assignable to type 'number | ActivityType'.\n` +
    `  Type '"COMPETING"' is not assignable to type 'number | ActivityType'.\n` +
    '\n' +
    '\x1B[7m36\x1B[0m                     type: config.activity.type,\n' +
    '\x1B[7m  \x1B[0m \x1B[91m                    ~~~~\x1B[0m\n' +
    '\n' +
    '  \x1B[96mnode_modules/discord.js/typings/index.d.ts\x1B[0m:\x1B[93m276\x1B[0m:\x1B[93m69\x1B[0m\n' +
    '    \x1B[7m276\x1B[0m   public setActivity(name: string | null, options?: { url?: string, type?: ActivityType | number }): Promise<Presence>;\n' +
    '    \x1B[7m   \x1B[0m \x1B[96m                                                                    ~~~~\x1B[0m\n' +
    "    The expected type comes from property 'type' which is declared here on type '{ url?: string; type?: number | ActivityType; }'\n" +
    "\x1B[96msrc/structures/QbotClient.ts\x1B[0m:\x1B[93m66\x1B[0m:\x1B[93m31\x1B[0m - \x1B[91merror\x1B[0m\x1B[90m TS2339: \x1B[0mProperty 'application' does not exist on type 'QbotClient'.\n" +
    '\n' +
    '\x1B[7m66\x1B[0m                 discordClient.application.commands.set(slashCommands);\n' +
    '\x1B[7m  \x1B[0m \x1B[91m                              ~~~~~~~~~~~\x1B[0m\n',
  diagnosticCodes: [ 2345, 2339, 2322, 2339 ]
}
exit status 1
 ^C
 
