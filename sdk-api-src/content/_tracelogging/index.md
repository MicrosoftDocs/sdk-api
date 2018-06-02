---
UID: TP:tracelogging
ms.assetid: 1bc44f9c-6d1d-3afa-9402-657cb5c8625e
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# TraceLogging



Overview of the TraceLogging technology.

To develop TraceLogging, you need these headers:

 * [traceloggingactivity.h](..\traceloggingactivity\index.md)
 * [traceloggingprovider.h](..\traceloggingprovider\index.md)

For the programming guide, see [TraceLogging](/windows/desktop/tracelogging).

## Functions

| Title   | Description   |
| ---- |:---- |
| [TraceLoggingProviderEnabled function](..\traceloggingprovider\nf-traceloggingprovider-traceloggingproviderenabled.md) | Indicates whether any sessions have subscribed to the provider. |
| [TraceLoggingProviderId function](..\traceloggingprovider\nf-traceloggingprovider-traceloggingproviderid.md) | Returns the provider ID that was specified in TRACELOGGING_DEFINE_PROVIDER. |
| [TraceLoggingRegister function](..\traceloggingprovider\nf-traceloggingprovider-traceloggingregister.md) | Registers a TraceLogging provider so that it can be used for to log events. |
| [TraceLoggingRegisterEx function](..\traceloggingprovider\nf-traceloggingprovider-traceloggingregisterex.md) | Registers a TraceLogging provider with callback so that it can be used for to log events. |
| [TraceLoggingSetInformation function](..\traceloggingprovider\nf-traceloggingprovider-traceloggingsetinformation.md) | Provides special-purpose information to the Event Tracing for Windows (ETW) runtime. |
| [TraceLoggingUnregister function](..\traceloggingprovider\nf-traceloggingprovider-traceloggingunregister.md) | Unregisters a TraceLogging provider. |

## Classes

| Title   | Description   |
| ---- |:---- |
| [TraceLoggingActivity class](..\traceloggingactivity\nl-traceloggingactivity-traceloggingactivity.md) | Provides support for logging ETW events during an activity. All events must be manually tagged or nested. |
| [TraceLoggingActivity class](..\traceloggingactivity\nl-traceloggingactivity-traceloggingactivity~r1.md) | Provides support for logging ETW events during an activity. All events must be manually tagged or nested. |
| [TraceLoggingThreadActivity class](..\traceloggingactivity\nl-traceloggingactivity-traceloggingthreadactivity.md) | Provides support for logging ETW events during an activity. Events will be automatically tagged with or nested in this activity. |
| [TraceLoggingThreadActivity class](..\traceloggingactivity\nl-traceloggingactivity-traceloggingthreadactivity~r1.md) | Provides support for logging ETW events during an activity. Events will be automatically tagged with or nested in this activity. |
| [TraceLoggingThreadActivityIdSetter class](..\traceloggingactivity\nl-traceloggingactivity-traceloggingthreadactivityidsetter.md) | Tags a thread with an activity id so ETW marks all events in that thread with the activity id. |
| [TraceLoggingThreadActivityIdSetter class](..\traceloggingactivity\nl-traceloggingactivity-traceloggingthreadactivityidsetter~r1.md) | Tags a thread with an activity id so ETW marks all events in that thread with the activity id. |

## Macros

| Title   | Description   |
| ---- |:---- |
| [TRACELOGGING_DECLARE_PROVIDER macro](..\traceloggingprovider\nf-traceloggingprovider-tracelogging_declare_provider.md) | Forward declares a global TraceLogging provider handle. |
| [TRACELOGGING_DEFINE_PROVIDER macro](..\traceloggingprovider\nf-traceloggingprovider-tracelogging_define_provider.md) | Allocates storage for a TraceLogging provider and creates a handle to the provider. |
| [TRACELOGGING_DEFINE_PROVIDER_STORAGE macro](..\traceloggingprovider\nf-traceloggingprovider-tracelogging_define_provider_storage.md) | Allocates storage for a TraceLogging provider. This macro should only be used for advanced scenarios. |
| [TraceLoggingBinary macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingbinary.md) | Wrapper macro for raw binary data. |
| [TraceLoggingChannel macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingchannel.md) | Wrapper macro for setting the event's channel. |
| [TraceLoggingCustom macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingcustom.md) | Wrapper macro for an event field packed using a custom serializer. |
| [TraceLoggingCustomAttribute macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingcustomattribute.md) | Wrapper macro for adding custom information about an event to the PDB. |
| [TraceLoggingDescription macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingdescription.md) | Wrapper macro for setting a description for an event. |
| [TraceLoggingEventTag macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingeventtag.md) | Wrapper macro for setting the event's tag(s). |
| [TraceLoggingFunction macro](..\traceloggingactivity\nf-traceloggingactivity-traceloggingfunction.md) | Creates a TraceLoggingThreadActivity named after the current function and writes a Start event for the activity. A Stop activity will be written at the end of the current scope. |
| [TraceLoggingKeyword macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingkeyword.md) | Wrapper macro for setting the event's keyword(s). |
| [TraceLoggingLevel macro](..\traceloggingprovider\nf-traceloggingprovider-tracelogginglevel.md) | Wrapper macro for setting the event's level. |
| [TraceLoggingOpcode macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingopcode.md) | Wrapper macro for setting the event's opcode. |
| [TraceLoggingOptionGroup macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingoptiongroup.md) | Wrapper macro for use in TRACELOGGING_DEFINE_PROVIDER to declare the GUID of the provider group that the provider is a member of. |
| [TraceLoggingSocketAddress macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingsocketaddress.md) | A wrapper macro that provides trace logging for socket addresses. |
| [TraceLoggingStruct macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingstruct.md) | Wrapper macro for defining a group of related fields in an event. |
| [TraceLoggingValue macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingvalue.md) | Wrapper macro for event fields. Automatically deduces value type. |
| [TraceLoggingWrite macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingwrite.md) | Emits an event. |
| [TraceLoggingWriteActivity macro](..\traceloggingprovider\nf-traceloggingprovider-traceloggingwriteactivity.md) | Emits an event with specific activity IDs. |
| [TraceLoggingWriteStart macro](..\traceloggingactivity\nf-traceloggingactivity-traceloggingwritestart.md) | Starts an activity and logs the start event. |
| [TraceLoggingWriteStop macro](..\traceloggingactivity\nf-traceloggingactivity-traceloggingwritestop.md) | Stops an activity and logs the stop event. |
| [TraceLoggingWriteTagged macro](..\traceloggingactivity\nf-traceloggingactivity-traceloggingwritetagged.md) | Logs an event with an associated ETW activity id. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [TraceLoggingActivity::Provider](..\traceloggingactivity\nf-traceloggingactivity-traceloggingactivity-provider.md) | Returns the handle to the TraceLogging provider associated with this activity. |
| [TraceLoggingActivity::SetRelatedActivityId(const GUID)](..\traceloggingactivity\nf-traceloggingactivity-traceloggingactivity-setrelatedactivityid(const guid).md) | Uses the unique identifier of an activity to set the related activity for this TraceLoggingActivity object. |
| [TraceLoggingActivity::SetRelatedActivityId](..\traceloggingactivity\nf-traceloggingactivity-traceloggingactivity-setrelatedactivityid.md) | Uses the unique identifier of an activity to set the related activity for this TraceLoggingActivity object. |
| [TraceLoggingActivity::SetRelatedActivity](..\traceloggingactivity\nf-traceloggingactivity-traceloggingactivity-setrelatedactivity.md) | Sets the related activity for this TraceLoggingActivity object. |
| [TraceLoggingActivity::TraceLoggingActivity(TraceLoggingActivity &&)](..\traceloggingactivity\nf-traceloggingactivity-traceloggingactivity-traceloggingactivity(traceloggingactivity &&).md) | Creates a new TraceLoggingActivity object. |
| [TraceLoggingActivity::TraceLoggingActivity](..\traceloggingactivity\nf-traceloggingactivity-traceloggingactivity-traceloggingactivity.md) | Creates a new TraceLoggingActivity object. |
| [TraceLoggingThreadActivity::Provider](..\traceloggingactivity\nf-traceloggingactivity-traceloggingthreadactivity-provider.md) | Returns the handle to the TraceLogging provider associated with this activity. |
| [TraceLoggingThreadActivity::TraceLoggingThreadActivity(TraceLoggingThreadActivity &&)](..\traceloggingactivity\nf-traceloggingactivity-traceloggingthreadactivity-traceloggingthreadactivity(traceloggingthreadactivity &&).md) | Initializes a new instance of the TraceLoggingThreadActivity class. |
| [TraceLoggingThreadActivity::TraceLoggingThreadActivity](..\traceloggingactivity\nf-traceloggingactivity-traceloggingthreadactivity-traceloggingthreadactivity.md) | Initializes a new instance of the TraceLoggingThreadActivity class. |
| [TraceLoggingThreadActivityIdSetter::TraceLoggingThreadActivityIdSetter(const GUID &)](..\traceloggingactivity\nf-traceloggingactivity-traceloggingthreadactivityidsetter-traceloggingthreadactivityidsetter(const guid &).md) | Creates a new TraceLoggingThreadActivityIdSetter object. |
| [TraceLoggingThreadActivityIdSetter::TraceLoggingThreadActivityIdSetter(const GUID)](..\traceloggingactivity\nf-traceloggingactivity-traceloggingthreadactivityidsetter-traceloggingthreadactivityidsetter(const guid).md) | Creates a new TraceLoggingThreadActivityIdSetter object. |
| [TraceLoggingThreadActivityIdSetter::TraceLoggingThreadActivityIdSetter](..\traceloggingactivity\nf-traceloggingactivity-traceloggingthreadactivityidsetter-traceloggingthreadactivityidsetter.md) | Creates a new TraceLoggingThreadActivityIdSetter object. |
| [TraceLoggingThreadActivityIdSetter::~TraceLoggingThreadActivityIdSetter](..\traceloggingactivity\nf-traceloggingactivity-traceloggingthreadactivityidsetter-~traceloggingthreadactivityidsetter.md) | Restores the original activity ID to the thread. |
