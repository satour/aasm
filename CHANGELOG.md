# CHANGELOG

## 4.9.0

 * add support for callback classes (`after` only) (see [issue #316](https://github.com/aasm/aasm/pull/316) for details, thanks to [@mlr](https://github.com/mlr))
 * allow easier extension of _AASM_ (utilising the idea of _ApplicationRecords_ from _Rails 5_) (see [issue #296](https://github.com/aasm/aasm/pull/296) for details, thanks to [@mlr](https://github.com/mlr))
 * support pessimistic locking for _ActiveRecord_ (see [issue #283](https://github.com/aasm/aasm/pull/283) for details, thanks to [@HoyaBoya](https://github.com/HoyaBoya))
 * fix: support database sharding for _ActiveRecord_ (see [issue #289](https://github.com/aasm/aasm/pull/289) for details, thanks to [@scambra](https://github.com/scambra))
 * fix: some issues with RubyMotion (see [issue #318](https://github.com/aasm/aasm/pull/318) for details, thanks to [@Infotaku](https://github.com/Infotaku))
 * fix: Rails generator now features the correct namespace (see [issue #328](https://github.com/aasm/aasm/pull/328) and [issue #329](https://github.com/aasm/aasm/pull/329) for details, thanks to [@anilmaurya](https://github.com/anilmaurya))


## 4.8.0

 * add support for [dynamoid](http://joshsymonds.com/Dynamoid/) (see [issue #300](https://github.com/aasm/aasm/pull/300) for details, thanks to [@LeeChSien](https://github.com/LeeChSien))
 * make compatible with [RubyMotion](http://www.rubymotion.com) (see [issue #315](https://github.com/aasm/aasm/pull/315) for details, thanks to [@Infotaku](https://github.com/Infotaku))
 * improve error handling in case of an exception during transitioning (see [issue #275](https://github.com/aasm/aasm/pull/275) for details, thanks to [@chriswoodrich](https://github.com/chriswoodrich))
 * rspec matcher `on_event` now supports arguments (see [issue #309](https://github.com/aasm/aasm/pull/309) for details, thanks to [@zacviandier](https://github.com/zacviandier))
 * fix: permitted states now respect guards (see [issue #308](https://github.com/aasm/aasm/pull/308) for details, thanks to [@eebs](https://github.com/eebs))
 * fix: reloading the env now doesn't add callbacks twice anymore (see [issue #311](https://github.com/aasm/aasm/pull/311) for details, thanks to [@lingceng](https://github.com/lingceng))

## 4.7.0

 * fix: allow :send as event name (see [issue #257](https://github.com/aasm/aasm/issues/257) for details)
 * add new callbacks: transactions, all events, ensure (see [issue #282](https://github.com/aasm/aasm/issues/282) for details, thanks to [@HoyaBoya](https://github.com/HoyaBoya))

## 4.6.0

 * fix: make sure the column is actually present for _ActiveRecord_ enums (see [issue #265](https://github.com/aasm/aasm/issues/265) and [issue #152](https://github.com/aasm/aasm/issues/152) for details, thanks to [@anilmaurya](https://github.com/anilmaurya))
 * add generators to configure active_record and mongoid after install (see [issue #261](https://github.com/aasm/aasm/issues/261) for details, thanks to [@anilmaurya](https://github.com/anilmaurya))

## 4.5.2

 * fix arity difference between Procs and lambdas (see [issue #293](https://github.com/aasm/aasm/issues/293) for details)

## 4.5.1

 * make sure to use override configuration options if state machine is defined more than once (see [issue #287](https://github.com/aasm/aasm/issues/287) for details)

## 4.5.0

 * add RSpec matchers `have_state`, `allow_event` and `allow_transition_to` (see [issue #147](https://github.com/aasm/aasm/issues/147) for details)
 * add RSpec matcher `transition_from` (see [issue #178](https://github.com/aasm/aasm/issues/178) for details, thanks to [@thomasstephane](https://github.com/thomasstephane))

## 4.4.1

 * add support for rejecting certain events on inspection (see [issue #272](https://github.com/aasm/aasm/issues/272)  for details, thanks to [@dubroe](https://github.com/dubroe))

## 4.4.0

 * add support global transation callbacks (see [issue #221](https://github.com/aasm/aasm/issues/221) and [issue #253](https://github.com/aasm/aasm/issues/253) for details)
 * add support (bugfix) for Mongoid >= 5.0 (see [issue #277](https://github.com/aasm/aasm/issues/277) and [issue #278](https://github.com/aasm/aasm/issues/278) for details)

## 4.3.0

 * add support for multiple state machines per class (see [issue #158](https://github.com/aasm/aasm/issues/158) and [issue #240](https://github.com/aasm/aasm/issues/240) for details)
    * special thanks to [@evadne](https://github.com/evadne) for testing this feature, and providing comments and patches (see [issue #245](https://github.com/aasm/aasm/issues/245) for details)

## 4.2.0

 * support turning off and on the configuration option for `no_direct_assignment` (see [issue #223](https://github.com/aasm/aasm/issues/223) for details)
 * event arguments are now passed to `:after_commit` callbacks as well (see [issue #238](https://github.com/aasm/aasm/pull/238), thanks to [@kuinak](https://github.com/kuinak))

## 4.1.1

 * support block notation for `:after_commit` event callbacks (see [issue #224](https://github.com/aasm/aasm/issues/224) for details)
 * event arguments are now passed to state callbacks as well (not only to event callbacks) (see [issue #219](https://github.com/aasm/aasm/issues/219), thanks to [@tobithiel](https://github.com/tobithiel))
 * `AASM::InvalidTransition` now references the current object (with the state machine) and the _AASM_ event name (see [issue #217](https://github.com/aasm/aasm/issues/217), thanks to [@awsmsrc](https://github.com/awsmsrc))
 * bugfix: do not update unloaded state for [Sequel](http://sequel.jeremyevans.net/) (see [issue #218](https://github.com/aasm/aasm/issues/218), thanks to [@godfat](https://github.com/godfat))

## 4.1.0

 * bugfix: initialize the aasm state column after initialization of the _Mongoid_ instance (see [issue #206](https://github.com/aasm/aasm/issues/206), thanks to [@Shwetakale ](https://github.com/Shwetakale ))
 * added support for mongomapper ORM (see [issue #203](https://github.com/aasm/aasm/issues/203), thanks to [@reidmorrison ](https://github.com/reidmorrison ))
 * `aasm_column` has been removed. Use `aasm.attribute_name` instead
 * `aasm_human_event_name` has been removed. Use `aasm.human_event_name` instead

## 4.0.8

 * bugfix: may_event_name? should return true or false only (see [issue #200](https://github.com/aasm/aasm/issues/200) for details)

## 4.0.7

 * bugfix: take private methods into account when checking for callbacks (see [issue #197](https://github.com/aasm/aasm/issues/197) for details)

## 4.0.6

 * bugfix: `false` is treated as uninitialised state (same as `nil`) (see [issue #195](https://github.com/aasm/aasm/issues/195) for details)
 * bugfix: an event's `:error` callback now retrieves all arguments passed to the event (see [issue #196](https://github.com/aasm/aasm/issues/196) for details)

## 4.0.5

 * bugfix: initialize the aasm state column after initialization of the _ActiveRecord_ instance only if the attribute has been loaded (see [issue #193](https://github.com/aasm/aasm/issues/193) for details)

## 4.0.4

 * corrected callback order in README
 * bugfix: initialize the aasm state column after initialization of the _ActiveRecord_ instance (see [issue #191](https://github.com/aasm/aasm/issues/191) for details)
 * bugfix: avoid Rails autoloading conflicts (see [issue #137](https://github.com/aasm/aasm/issues/137) and [issue #139](https://github.com/aasm/aasm/issues/139) for details)

## 4.0.3

 * bugfix: fire guards only once per transition, part 2 (see [issue #187](https://github.com/aasm/aasm/issues/187) for details)
 * `aasm_column` is deprecated. Use `aasm.attribute_name` instead

## 4.0.2

 * bugfix: really support block-guards (defined within a transition block) (see [issue #186](https://github.com/aasm/aasm/issues/186) for details)

## 4.0.1

 * fire guards only once per transition (see [issue #184](https://github.com/aasm/aasm/issues/184) for details)
 * `aasm_human_event_name` is deprecated, use `aasm.human_event_name` instead

## 4.0.0

 * support `if` and `unless` guard syntax: (see [issue #179](https://github.com/aasm/aasm/issues/179) and [issue #181](https://github.com/aasm/aasm/issues/181)), thanks to [@bigtunacan](https://github.com/bigtunacan)
 * may configure to not allow direct assignment for persisted AASM models (see [issue #53](https://github.com/aasm/aasm/issues/53))
 * **DSL change**: callbacks don't require `to_state` parameter anymore, but still support it
   (closing issues
   [#11](https://github.com/aasm/aasm/issues/11),
   [#58](https://github.com/aasm/aasm/issues/58) and
   [#80](https://github.com/aasm/aasm/issues/80)
   thanks to [@ejlangev](https://github.com/ejlangev))
 * **DSL change**: `after_commit` hooks are now event-based (see [issue #112](https://github.com/aasm/aasm/issues/112))
 * **DSL change**: event and state callbacks have been re-ordered; state callbacks are not run anymore if any guard fails
 * **DSL change**: `:on_transition` renamed to `:after`
 * **DSL change**: `:on_transition` renamed to `:after`
 * **DSL change**: transition `:after` binding changed (see [issue #59](https://github.com/aasm/aasm/issues/59), thanks to [@stiff](https://github.com/stiff))
 * **DSL change**: instance-based events inspection now returns event instances (instead of the event names as symbol)
 * **DSL change**: instance-based permissible_events has been removed in favor or events(:permissible => true)
 * **DSL change**: class-based events now returns a list of Event instances (instead of a hash with event names as keys)
 * **DSL change**: renamed permissible states and events to permitted states events
 * removed deprecated methods (mostly the ones prefixed with `aasm_`)

## 3.4.0

 * allow retrieving the current event (`aasm.current_event`) (see [issue #159](https://github.com/aasm/aasm/issues/159) and [issue #168](https://github.com/aasm/aasm/issues/168))

## 3.3.3

 * bugfix: support reloading development environment in Rails (see [issue #148](https://github.com/aasm/aasm/issues/148))

## 3.3.2

 * bugfix: avoid conflicts with `failed` and `fired` event names (see [issue #157](https://github.com/aasm/aasm/issues/157)), thanks to [@MichaelXavier](https://github.com/MichaelXavier)
 * bugfix: not using transactions unless saving to the database (see [issue #162](https://github.com/aasm/aasm/issues/162) and [issue #164](https://github.com/aasm/aasm/issues/164)), thanks to [@roberthoner](https://github.com/roberthoner)
 * bugfix: `after_commit` should only run if saving to the database (see [issue #151](https://github.com/aasm/aasm/issues/151)), thanks to [@ivantsepp](https://github.com/ivantsepp)

## 3.3.1

 * bugfix: permissible events will respect given `guards` (see [issue #150](https://github.com/aasm/aasm/issues/150))

## 3.3.0

 * support for Rails 4.1 enum fields (see [issue #124](https://github.com/aasm/aasm/issues/124), thanks to [@bkon](https://github.com/bkon))
 * bugfix: allow lazy-evaluation for Rails 3 scopes (see [issue #144](https://github.com/aasm/aasm/issues/144), thanks to [@laurens](https://github.com/laurens))

## 3.2.1

 * bugfix: permissible_events and events did not contain events with an empty "from" transition (see [issue #140](https://github.com/aasm/aasm/issues/140) and [issue #141](https://github.com/aasm/aasm/issues/141), thanks to [@daniel-rikowski](https://github.com/daniel-rikowski))

## 3.2.0

 * support [Sequel](http://sequel.jeremyevans.net/) (see [issue #119](https://github.com/aasm/aasm/issues/119), thanks to [@godfat](https://github.com/godfat))
 * may not fire an unknown event (see [issue #128](https://github.com/aasm/aasm/issues/128)

## 3.1.1

 * bugfix: don't require ActiveRecord for localizing AASM event and state name (see [issue #113](https://github.com/aasm/aasm/issues/113), thanks to [@silentshade](https://github.com/silentshade))

## 3.1.0

 * validating the current state (see [issue #95](https://github.com/aasm/aasm/issues/95), thanks to [@ivantsepp](https://github.com/ivantsepp))
 * allow configuring behavior of nested transactions (see [issue #107](https://github.com/aasm/aasm/issues/107))
 * support multiple guards per transition
 * support event guards (see [issue #85](https://github.com/aasm/aasm/issues/85))
 * support reading from- and to-state during on_transition callback (see [issue #100](https://github.com/aasm/aasm/issues/100))

## 3.0.26

 * support state.human_name (aliased to state.localized_name) (see [issue #105](https://github.com/aasm/aasm/issues/105))

## 3.0.25

 * initialize the state even if validation is skipped (for ActiveRecord and Mongoid persistence) (see [issue #103](https://github.com/aasm/aasm/issues/103), thanks to [@vfonic](https://github.com/vfonic) and [@aaronklaassen](https://github.com/aaronklaassen))

## 3.0.24

 * added support for event blocks (thanks to [@Intrepidd](https://github.com/Intrepidd))

## 3.0.23

 * added support for `after_commit` callback (transaction support) (thanks to [@tisba](https://github.com/tisba))

## 3.0.22

 * fixed [issue 88](https://github.com/aasm/aasm/issues/88): wrong number of arguments for transaction method

## 3.0.21

 * support nested ActiveRecord transactions ([@ozeias](https://github.com/ozeias))
 * allow overwriting of events, can be very useful with inheritance ([@Intrepidd](https://github.com/Intrepidd))

## 3.0.20

 * added configuration option to disable automatic scope creation

## 3.0.19

 * fixed deprecation warning with *Rails 4* (`Relation#update_all` with conditions is deprecated)
 * fixing [issue #69](https://github.com/aasm/aasm/issues/69) ( *ActiveRecord* scopes are not chainable)

## 3.0.18

 * fixing [issue #66](https://github.com/aasm/aasm/issues/66) (state methods not reflecting the current state)

## 3.0.17

 * supporting instance level inspection for states (including permissible state, see [issue #54](https://github.com/aasm/aasm/issues/54))
 * added autocreation of constants for each state ([@jherdman](https://github.com/jherdman))

## 3.0.16

 * added autocreation of state scopes for Mongoid (thanks to [@jonnyshields](https://github.com/johnnyshields))

## 3.0.15

 * added support for localized state names (on a class level, like `Record.aasm.states.map(&:localized_name)`)

## 3.0.14

 * supporting event inspection for to-states transitions (`Event#transitions_to_state?`)

## 3.0.13

 * supporting *ActiveRecord* transactions when firing an event

## 3.0.12

 * `aasm_from_states_for_state` now supports to filter for specific transition

## 3.0.11

 * added class method `aasm_from_states_for_state` to retrieve all from states (regarding transitions) for a given state

## 3.0.10

 * added support for transitions from all other states (thanks to [@swrobel](https://github.com/swrobel))

## 3.0.9

 * guard checks (e.g. `may_edit?`) now support guard parameters as well

## 3.0.8

 * fixed issue with generating docs using yard

## 3.0.7

 * removed deprecation warning when localizing aasm state names (look at [issue #38](https://github.com/rubyist/aasm/issues/38) for details)

## 3.0.6

 * bugfix: if configured to skip validation the code does not validate anymore

## 3.0.5

 * bugfix: get rid of error with old rubygems versions

## 3.0.4

 * bugfix: Subclasses of aasm-enabled classes don't lose settings anymore (thanks to codez)

## 3.0.3

 * bugfix: ActiveRecord scopes are generated when using the new DSL

## 3.0.2

 * ActiveRecord persistence can ignore validation when trying to save invalid models

## 3.0.1

 * added support for Mongoid (Thanks, Michał Taberski)

## 3.0.0

 * switched documentation to the new DSL
 * whiny transactions: by default, raise an exception if an event transition is not possible
 * you may disable whiny transactions

## 2.4.0

 * supporting new DSL (which is much shorter)

## 2.3.1

 * bugfix: avoid naming conflict with i18n

## 2.3.0

 * supporting i18n
 * supporting regular expressions for hash values and strings

