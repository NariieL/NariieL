![SOZFond5](https://user-images.githubusercontent.com/104008465/206195637-86e4b31b-146c-44b5-b0e9-05b245faeb61.png)

<p align="center">
Developed especially for the Zerator community.
</p>

![SOZ - Main objectives ](https://user-images.githubusercontent.com/104008465/164983461-c2d93179-9df2-464b-934c-4c3903a87451.png)
The main goal of SOZ development is to **revamp the various primary mechanics used by players.** This desire to improve the landscape has pushed us to review **the ergonomics of several interactions with a point of honor**, even going so far as to review the primary interactions such as the exchange between players, the use of chests, parking lots, and many other things.

In order to make this dream come true, we had to force ourselves to **develop everything we could from scratch**, while making less use of what already exists for free, developed by a ton of developers with the goal of helping the community. **Allowing us to ignore all paid resources.**

The other goal of SOZ is to **offer a "Click & Host Server"**, but in all honesty, this is very difficult and our V1 will not allow this. **However, we will force ourselves to improve this until we can really offer this to you.**

Also, we count on the participation of the community. **We may not be the best, but together we can be.** Providing quality development that can improve all of our servers should be the primary goal of any developer with a community. **By creating SOZ, we want to allow any developer to take what we have developed and improve your respective servers.** At the same time helping SOZ to grow in order to contribute to the war effort.

![SOZ - Key Feature ](https://user-images.githubusercontent.com/104008465/164982666-ec501b93-94db-4773-83a4-0f8f0a96e7c5.png)
**Exhaustive list of what SOZ offers:**
> Use of a QB base that will disappear in V2.

> Fourteen different companies, with their own gameplay mechanics. Each of them having a dependence on another one in order to create open circuits of RôlePlay. (Example: Gas stations are emptied to force to be used, as well as banks and ATM. Asking Players to fill these. )

> A system of pollution and deforestation. If the company doesn't charge the electric stations, the city goes into blackout. If it produces too much, San Andreas becomes polluted.

> BTarget improvement, allowing to add any interaction.

> Use of safes simultaneously, all separate.

> A custom VOIP Mumble.

> Multiple vehicle exits for parking, garages and companies.

> Drag-and-drop inventory to improve usability. Accompanied by over two hundred objects with their own icons created by the SOZ community.

> A modern handmade phone, in partnership with FailyV.

> Free mappings created by our team, as well as map modifications added.

> A hundred of apartments, all ready to use.

*Note : Some mapping are actually delete from the OpenSource because they're not as our own propriety. They will be replace asap. So you need to relocalise some safes and interactions, like the LSPD office.*

![SOZ - Major credits ](https://user-images.githubusercontent.com/104008465/164984759-fea538fe-cf20-48bc-afd0-45cb96c4c7ae.png)
**We would like to thank all the creators who are offering some of their creations to the community for free. Whether it is on [5Mod](https://fr.gta5-mods.com/) or on the [FiveM](https://forum.cfx.re/c/development/releases/7/l/latest) website.** It is also due to you that all the servers exist ! Thanks to you, you inspired us to make SOZ completely free.

Some of these free components are used on SOZ, such as clothes and female haircuts. Even though this represents only 10% of the development, it is important to note that no, the server is not yet fully independent and homegrown. We strive to replace anything we use that does not come from our own hands as soon as possible, and we thank all those creators from the bottom of our hearts.

All contributors to the project will be notified in a list.

![SOZ - Using the server_](https://user-images.githubusercontent.com/104008465/206203151-701a8669-b4dc-479c-978a-8498b8c6129d.png)

### Requirements
 * NodeJS: to compile the code and migrate the database
 * MySQL/MariaDB: to store the data
 * Loki: to store the logs (Optional)
 * Prometheus: to store the metrics (Optional)

### Prepare and configure the server
 * Clone the repository: `git clone https://github.com/SOZ-Faut-etre-Sub/SOZ-FiveM-Server.git`
 * Copy the `env.cfg-dist` file to `env.cfg` and fill / replace any necessary values (like your database credentials)
 * Copy the `resources/[soz]/soz-core/.env-dist` file to `resources/[soz]/soz-core/.env` and fill / replace any necessary values (like your database credentials)
 * Compile the resources core and phone:
   ```
   cd resources/[soz]/soz-core && yarn install && yarn build
   cd resources/[soz]/soz-phone && yarn install && yarn build
   ```
 * Migrate the database:
   ```
   cd resources/[soz]/soz-core && yarn run prisma migrate deploy
   ```
 * If you want to run in "production" mode copy the `modules-prod.cfg` file to `modules.cfg`
 * If you want to run in "test" mode copy the `modules-prod.cfg` file to `modules.cfg`

### Running the server
Once everything is configured, [you can run the server by using the FXServer executable](https://docs.fivem.net/docs/server-manual/setting-up-a-server-vanilla/)

On Windows:
```
C:\FXServer\server\FXServer.exe +exec server.cfg
```

On Linux:
```
bash ~/FXServer/server/run.sh +exec server.cfg
```

### Data
This repository does not propose, yet, any base data (like vehicles, weapons, fuel stations, dealership, etc ....), you must use the inject your own data into
the database at the moment.

We want to provide a tool / base data set to do that, you can contribute to help us to do that.

![SOZ - Issues   Pull requests_](https://user-images.githubusercontent.com/104008465/206208630-bf79fd74-d6e8-4b67-821d-dd3080306b8e.png)
Contribution is welcome, but you must follow the rules below:

* You must follow the [code of conduct](CODE_OF_CONDUCT.md)
* If you are a user having problems with a server that is running this code, please contact the server owner, do not report an issue here.
* Issues must only be used by developers or administrators of servers that want to report a bug with the code source, or propose a feature.
* You must provide a minimum of information, this place is not a support forum, it's a discussion place for developers.
* If you want to contribute, read the [INTERNAL.md](INTERNAL.md) file before contributing, as it allow to understand how the code works and current vision of the project.

**Any issue or pull request that does not respect these rules will be closed without any warning.**

This repository is an extract of our internal repository, pull requests will be merged in our internal repository and then pushed to this repository automatically.
This means that you will not see your pull request merged here, and we will close them once they are merged in our internal repository.

Don't worry you will still be credited as a contributor, and your name will appear in this repository, but you will not see your pull request merged here.
