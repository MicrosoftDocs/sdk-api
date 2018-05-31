---
UID: TP:winsync
ms.assetid: ee92abfb-a568-3036-bd81-7498365db57b
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# Windows Sync



Overview of the Windows Sync technology.

To develop Windows Sync, you need these headers:

 * [syncregistration.h](..\syncregistration\index.md)
 * [winsync.h](..\winsync\index.md)

For the programming guide, see [Windows Sync](/previous-versions/windows/desktop/winsync).

## Structures

| Title   | Description   |
| ---- |:---- |
| [_ID_PARAMETERS structure](..\winsync\ns-winsync-_id_parameters.md) | Represents the format schema for the group of IDs that are used to identify entities in a synchronization session. |
| [_ID_PARAMETER_PAIR structure](..\winsync\ns-winsync-_id_parameter_pair.md) | Represents the format of a synchronization entity ID. |
| [_SYNC_RANGE structure](..\winsync\ns-winsync-_sync_range.md) | Represents a range of item IDs. |
| [_SYNC_SESSION_STATISTICS structure](..\winsync\ns-winsync-_sync_session_statistics.md) | Represents statistics about a single, unidirectional synchronization session. |
| [_SYNC_TIME structure](..\winsync\ns-winsync-_sync_time.md) | Represents a date-and-time value. |
| [_SYNC_VERSION structure](..\winsync\ns-winsync-_sync_version.md) | Represents a version for an item or a change unit. |
| [_SyncProviderConfigUIConfiguration structure](..\syncregistration\ns-syncregistration-_syncproviderconfiguiconfiguration.md) | Represents the information for a synchronization provider configuration UI. |
| [_SyncProviderConfiguration structure](..\syncregistration\ns-syncregistration-_syncproviderconfiguration.md) | Represents the information for a synchronization provider configuration. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [__MIDL___MIDL_itf_syncregistration_0000_0007_0001 enumeration](..\syncregistration\ne-syncregistration-__midl___midl_itf_syncregistration_0000_0007_0001.md) | Represents the different types of synchronization registration events. |
| [__MIDL___MIDL_itf_winsync_0000_0000_0001 enumeration](..\winsync\ne-winsync-__midl___midl_itf_winsync_0000_0000_0001.md) | Represents the role of a provider, relative to the other provider in the synchronization session. |
| [__MIDL___MIDL_itf_winsync_0000_0000_0002 enumeration](..\winsync\ne-winsync-__midl___midl_itf_winsync_0000_0000_0002.md) | Represents the options for the concurrency conflict resolution policy to use for the synchronization session. |
| [__MIDL___MIDL_itf_winsync_0000_0000_0003 enumeration](..\winsync\ne-winsync-__midl___midl_itf_winsync_0000_0000_0003.md) | Represents the stages of a synchronization session. |
| [__MIDL___MIDL_itf_winsync_0000_0000_0004 enumeration](..\winsync\ne-winsync-__midl___midl_itf_winsync_0000_0000_0004.md) | Represents the action to be taken by an application in response to ISyncCallback |
| [__MIDL___MIDL_itf_winsync_0000_0000_0005 enumeration](..\winsync\ne-winsync-__midl___midl_itf_winsync_0000_0000_0005.md) | Represents actions that are taken to resolve a specific concurrency conflict. |
| [__MIDL___MIDL_itf_winsync_0000_0000_0006 enumeration](..\winsync\ne-winsync-__midl___midl_itf_winsync_0000_0000_0006.md) | Represents types of statistics that convey information about a component. |
| [__MIDL___MIDL_itf_winsync_0000_0000_0007 enumeration](..\winsync\ne-winsync-__midl___midl_itf_winsync_0000_0000_0007.md) | Represents the version of Microsoft Sync Framework that a particular component is compatible with. |
| [__MIDL___MIDL_itf_winsync_0000_0000_0008 enumeration](..\winsync\ne-winsync-__midl___midl_itf_winsync_0000_0000_0008.md) | Indicates the type of information that is included in a change batch during filtered synchronization. |
| [__MIDL___MIDL_itf_winsync_0000_0000_0011 enumeration](..\winsync\ne-winsync-__midl___midl_itf_winsync_0000_0000_0011.md) | Represents the possible results when a knowledge cookie is compared with a knowledge object by using ISyncKnowledge2 |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IAsynchronousDataRetriever interface](..\winsync\nn-winsync-iasynchronousdataretriever.md) | Represents the mechanism by which the destination provider asynchronously retrieves item data from the source provider. |
| [IChangeConflict interface](..\winsync\nn-winsync-ichangeconflict.md) | Represents a conflict between two items. |
| [IChangeUnitException interface](..\winsync\nn-winsync-ichangeunitexception.md) | Represents a change unit to exclude from a knowledge object. |
| [IChangeUnitListFilterInfo interface](..\winsync\nn-winsync-ichangeunitlistfilterinfo.md) | Represents a filter that can be used to control which change units are included for items in an ISyncChangeBatch object. |
| [IClockVector interface](..\winsync\nn-winsync-iclockvector.md) | Represents a clock vector in a knowledge structure. |
| [IClockVectorElement interface](..\winsync\nn-winsync-iclockvectorelement.md) | Represents a clock vector element of a knowledge structure. |
| [IConstructReplicaKeyMap interface](..\winsync\nn-winsync-iconstructreplicakeymap.md) | Adds entries to an IReplicaKeyMap object. |
| [ICoreFragment interface](..\winsync\nn-winsync-icorefragment.md) | Represents knowledge of all items in the scope for a specific set of change units. |
| [ICoreFragmentInspector interface](..\winsync\nn-winsync-icorefragmentinspector.md) | Enumerates the ICoreFragment objects that are contained in a knowledge object. |
| [IDataRetrieverCallback interface](..\winsync\nn-winsync-idataretrievercallback.md) | Represents methods that an IAsynchronousDataRetriever object can call to indicate that processing has been completed on an IAsynchronousDataRetriever method. |
| [IEnumChangeUnitExceptions interface](..\winsync\nn-winsync-ienumchangeunitexceptions.md) | Enumerates change unit exceptions that are stored in a knowledge object. |
| [IEnumClockVector interface](..\winsync\nn-winsync-ienumclockvector.md) | Enumerates the clock vector elements that are stored in a clock vector. |
| [IEnumFeedClockVector interface](..\winsync\nn-winsync-ienumfeedclockvector.md) | Enumerates the clock vector elements that are stored in a clock vector that contains FeedSync information. |
| [IEnumRangeExceptions interface](..\winsync\nn-winsync-ienumrangeexceptions.md) | Enumerates range exceptions that are stored in a knowledge object. |
| [IEnumSingleItemExceptions interface](..\winsync\nn-winsync-ienumsingleitemexceptions.md) | Enumerates single-item exceptions that are stored in a knowledge object. |
| [IEnumSyncChangeUnits interface](..\winsync\nn-winsync-ienumsyncchangeunits.md) | Enumerates a list of change units. |
| [IEnumSyncChanges interface](..\winsync\nn-winsync-ienumsyncchanges.md) | Enumerates a list of item changes. |
| [IEnumSyncProviderConfigUIInfos interface](..\syncregistration\nn-syncregistration-ienumsyncproviderconfiguiinfos.md) | Enumerates ISyncProviderConfigUIInfo objects that contain configuration UI information used to build and register a synchronization provider. |
| [IEnumSyncProviderInfos interface](..\syncregistration\nn-syncregistration-ienumsyncproviderinfos.md) | Enumerates ISyncProviderInfo objects that contain the information used to create an instance of a synchronization provider. |
| [IFeedClockVector interface](..\winsync\nn-winsync-ifeedclockvector.md) | Represents a clock vector that contains FeedSync information. |
| [IFeedClockVectorElement interface](..\winsync\nn-winsync-ifeedclockvectorelement.md) | Represents a clock vector element that contains FeedSync information. |
| [IFilterRequestCallback interface](..\winsync\nn-winsync-ifilterrequestcallback.md) | Mediates filter negotiation between a destination provider and a source provider. |
| [IForgottenKnowledge interface](..\winsync\nn-winsync-iforgottenknowledge.md) | Represents knowledge that has been forgotten because of tombstone cleanup. |
| [IKnowledgeSyncProvider interface](..\winsync\nn-winsync-iknowledgesyncprovider.md) | Represents a synchronization provider that uses knowledge to perform synchronization. |
| [ILoadChangeContext interface](..\winsync\nn-winsync-iloadchangecontext.md) | Represents information about a change to be loaded from the item store. |
| [IProviderConverter interface](..\winsync\nn-winsync-iproviderconverter.md) | When implemented by a derived class, represents an object that can convert an ISyncProvider object to an IKnowledgeSyncProvider object. |
| [IRangeException interface](..\winsync\nn-winsync-irangeexception.md) | Represents an item ID range to exclude from a knowledge object. |
| [IRecoverableError interface](..\winsync\nn-winsync-irecoverableerror.md) | Represents a recoverable error that occurred when an item was loaded or when an item was saved. |
| [IRecoverableErrorData interface](..\winsync\nn-winsync-irecoverableerrordata.md) | Represents information about a recoverable error. |
| [IRegisteredSyncProvider interface](..\syncregistration\nn-syncregistration-iregisteredsyncprovider.md) | Represents a registered synchronization provider. This interface is implemented by the writer of a synchronization provider. |
| [IReplicaKeyMap interface](..\winsync\nn-winsync-ireplicakeymap.md) | Represents a mapping between replica keys and replica IDs. |
| [IRequestFilteredSync interface](..\winsync\nn-winsync-irequestfilteredsync.md) | When implemented by a derived class, represents a destination provider that can specify a filter to be used by the source provider during change enumeration. |
| [ISingleItemException interface](..\winsync\nn-winsync-isingleitemexception.md) | Represents an item to exclude from a knowledge object. |
| [ISupportFilteredSync interface](..\winsync\nn-winsync-isupportfilteredsync.md) | When implemented by a derived class, represents a source provider that supports filtered change enumeration, and that can negotiate the type of filter that is used. |
| [ISupportLastWriteTime interface](..\winsync\nn-winsync-isupportlastwritetime.md) | Represents a synchronization provider that is able to report the date and time when an item or change unit was last changed. This ability is useful to an application that implements last-writer-wins conflict resolution. |
| [ISyncCallback interface](..\winsync\nn-winsync-isynccallback.md) | Represents application callbacks that are used to notify the application of synchronization events. |
| [ISyncCallback2 interface](..\winsync\nn-winsync-isynccallback2.md) | Represents additional application callbacks that are used to notify the application of synchronization events. |
| [ISyncChange interface](..\winsync\nn-winsync-isyncchange.md) | Represents a change to an item. |
| [ISyncChangeBatch interface](..\winsync\nn-winsync-isyncchangebatch.md) | Represents metadata for a set of changes. |
| [ISyncChangeBatchAdvanced interface](..\winsync\nn-winsync-isyncchangebatchadvanced.md) | Represents additional information about a set of changes. |
| [ISyncChangeBatchBase interface](..\winsync\nn-winsync-isyncchangebatchbase.md) | Represents metadata for a set of changes. |
| [ISyncChangeBatchBase2 interface](..\winsync\nn-winsync-isyncchangebatchbase2.md) | Represents additional capabilities of an ISyncChangeBatchBase object. |
| [ISyncChangeBatchWithPrerequisite interface](..\winsync\nn-winsync-isyncchangebatchwithprerequisite.md) | Represents metadata about a change batch that is based on the prerequisite knowledge associated with the change batch. |
| [ISyncChangeBuilder interface](..\winsync\nn-winsync-isyncchangebuilder.md) | Provides additional data for an item change. |
| [ISyncChangeUnit interface](..\winsync\nn-winsync-isyncchangeunit.md) | Represents a change to a change unit that is contained in an item. |
| [ISyncChangeWithPrerequisite interface](..\winsync\nn-winsync-isyncchangewithprerequisite.md) | Represents metadata about a change that is based on the prerequisite knowledge that is associated with the change. |
| [ISyncFilterInfo interface](..\winsync\nn-winsync-isyncfilterinfo.md) | Represents information about a filter that is used to control the data that is included in an ISyncChangeBatch object. |
| [ISyncFilterInfo2 interface](..\winsync\nn-winsync-isyncfilterinfo2.md) | Represents additional information about a filter that can be used to control which changes are included in an ISyncChangeBatch object. |
| [ISyncFullEnumerationChange interface](..\winsync\nn-winsync-isyncfullenumerationchange.md) | Represents additional information about an ISyncChange object during recovery synchronization. |
| [ISyncFullEnumerationChangeBatch interface](..\winsync\nn-winsync-isyncfullenumerationchangebatch.md) | Represents the metadata for a set of changes that is created as part of a recovery synchronization. |
| [ISyncKnowledge interface](..\winsync\nn-winsync-isyncknowledge.md) | Represents knowledge that a replica has about its item store. |
| [ISyncKnowledge2 interface](..\winsync\nn-winsync-isyncknowledge2.md) | Represents additional information about the knowledge that a replica has about its item store. |
| [ISyncProvider interface](..\winsync\nn-winsync-isyncprovider.md) | Represents a synchronization provider that can be used by a synchronization session to synchronize data with another synchronization provider. |
| [ISyncProviderConfigUI interface](..\syncregistration\nn-syncregistration-isyncproviderconfigui.md) | Represents configuration UI information used to build and register a synchronization provider. |
| [ISyncProviderConfigUIInfo interface](..\syncregistration\nn-syncregistration-isyncproviderconfiguiinfo.md) | Represents the information and properties needed to create an instance of a synchronization provider configuration UI. |
| [ISyncProviderInfo interface](..\syncregistration\nn-syncregistration-isyncproviderinfo.md) | Represents the information and properties needed to create an instance of a synchronization provider. |
| [ISyncProviderRegistration interface](..\syncregistration\nn-syncregistration-isyncproviderregistration.md) | Represents synchronization provider registration. |
| [ISyncRegistrationChange interface](..\syncregistration\nn-syncregistration-isyncregistrationchange.md) | Represents a change to the registration of a synchronization provider or a synchronization provider configuration UI. The changes are reported as registration events. |
| [ISyncSessionExtendedErrorInfo interface](..\winsync\nn-winsync-isyncsessionextendederrorinfo.md) | Represents information about which provider caused synchronization to fail. |
| [ISyncSessionState interface](..\winsync\nn-winsync-isyncsessionstate.md) | Represents information about the current synchronization session. |
| [ISyncSessionState2 interface](..\winsync\nn-winsync-isyncsessionstate2.md) | Represents additional information about the current synchronization session. |
| [ISynchronousDataRetriever interface](..\winsync\nn-winsync-isynchronousdataretriever.md) | Represents the mechanism by which the destination provider retrieves item data from the source provider. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IAsynchronousDataRetriever::GetIdParameters](..\winsync\nf-winsync-iasynchronousdataretriever-getidparameters.md) | Gets the ID format schema of the provider. |
| [IAsynchronousDataRetriever::LoadChangeData](..\winsync\nf-winsync-iasynchronousdataretriever-loadchangedata.md) | Retrieves item data for a change. |
| [IAsynchronousDataRetriever::RegisterCallback](..\winsync\nf-winsync-iasynchronousdataretriever-registercallback.md) | Registers a callback interface that will be called by the IAsynchronousDataRetriever object when an asynchronous method finishes processing. |
| [IAsynchronousDataRetriever::RevokeCallback](..\winsync\nf-winsync-iasynchronousdataretriever-revokecallback.md) | Indicates that the IAsynchronousDataRetriever object must no longer use the specified callback interface and must release any references to it. |
| [IChangeConflict::GetDestinationProviderConflictingChange](..\winsync\nf-winsync-ichangeconflict-getdestinationproviderconflictingchange.md) | Gets the change metadata from the destination provider. |
| [IChangeConflict::GetDestinationProviderConflictingData](..\winsync\nf-winsync-ichangeconflict-getdestinationproviderconflictingdata.md) | Gets an object that can be used to retrieve item data for the change item from the destination replica. |
| [IChangeConflict::GetResolveActionForChangeUnit](..\winsync\nf-winsync-ichangeconflict-getresolveactionforchangeunit.md) | Gets the conflict resolution action for the conflicting change unit change. |
| [IChangeConflict::GetResolveActionForChange](..\winsync\nf-winsync-ichangeconflict-getresolveactionforchange.md) | Gets the conflict resolution action for the conflict. |
| [IChangeConflict::GetSourceProviderConflictingChange](..\winsync\nf-winsync-ichangeconflict-getsourceproviderconflictingchange.md) | Gets the change metadata from the source provider. |
| [IChangeConflict::GetSourceProviderConflictingData](..\winsync\nf-winsync-ichangeconflict-getsourceproviderconflictingdata.md) | Gets an object that can be used to retrieve item data for the change item from the source replica. |
| [IChangeConflict::SetResolveActionForChangeUnit](..\winsync\nf-winsync-ichangeconflict-setresolveactionforchangeunit.md) | Sets a conflict resolution action for the conflicting change unit change. |
| [IChangeConflict::SetResolveActionForChange](..\winsync\nf-winsync-ichangeconflict-setresolveactionforchange.md) | Sets a conflict resolution action for the conflict. |
| [IChangeUnitException::GetChangeUnitId](..\winsync\nf-winsync-ichangeunitexception-getchangeunitid.md) | Gets the change unit ID for the change unit that is associated with the exception. |
| [IChangeUnitException::GetClockVector](..\winsync\nf-winsync-ichangeunitexception-getclockvector.md) | Gets the clock vector that is associated with this exception. |
| [IChangeUnitException::GetItemId](..\winsync\nf-winsync-ichangeunitexception-getitemid.md) | Gets the item ID for the item that contains the change unit that is associated with the exception. |
| [IChangeUnitListFilterInfo::GetChangeUnitIdCount](..\winsync\nf-winsync-ichangeunitlistfilterinfo-getchangeunitidcount.md) | Gets the number of change unit IDs that define the filter. |
| [IChangeUnitListFilterInfo::GetChangeUnitId](..\winsync\nf-winsync-ichangeunitlistfilterinfo-getchangeunitid.md) | Gets the change unit ID that is stored at the specified index in the array of change unit IDs that define the filter. |
| [IChangeUnitListFilterInfo::Initialize](..\winsync\nf-winsync-ichangeunitlistfilterinfo-initialize.md) | Initializes a new instance of the IChangeUnitListFilterInfo class that contains the specified array of change unit IDs. |
| [IClockVector::GetClockVectorElementCount](..\winsync\nf-winsync-iclockvector-getclockvectorelementcount.md) | Gets the number of elements that are contained in the clock vector. |
| [IClockVector::GetClockVectorElements](..\winsync\nf-winsync-iclockvector-getclockvectorelements.md) | Returns an enumerator that iterates through the clock vector elements. |
| [IClockVectorElement::GetReplicaKey](..\winsync\nf-winsync-iclockvectorelement-getreplicakey.md) | Gets the replica key for the replica that is associated with this clock vector element. |
| [IClockVectorElement::GetTickCount](..\winsync\nf-winsync-iclockvectorelement-gettickcount.md) | Gets the tick count that defines the upper bound on the range of tick counts that are contained in this clock vector element. |
| [IConstructReplicaKeyMap::FindOrAddReplica](..\winsync\nf-winsync-iconstructreplicakeymap-findoraddreplica.md) | Adds entries to or finds entries in an IReplicaKeyMap object. |
| [ICoreFragment::GetColumnCount](..\winsync\nf-winsync-icorefragment-getcolumncount.md) | Gets the number of columns that are contained in this knowledge fragment. |
| [ICoreFragment::GetRangeCount](..\winsync\nf-winsync-icorefragment-getrangecount.md) | Gets the number of ranges that are contained in this knowledge fragment. |
| [ICoreFragment::NextColumn](..\winsync\nf-winsync-icorefragment-nextcolumn.md) | Returns the next change unit ID in the set of change unit IDs that this knowledge fragment applies to. |
| [ICoreFragment::NextRange](..\winsync\nf-winsync-icorefragment-nextrange.md) | Returns the next range that is contained in this knowledge fragment, and the clock vector that defines what is known about the items in the range. |
| [ICoreFragment::Reset](..\winsync\nf-winsync-icorefragment-reset.md) | Resets both the column and range enumerators to the beginning of their respective sets. |
| [ICoreFragmentInspector::NextCoreFragments](..\winsync\nf-winsync-icorefragmentinspector-nextcorefragments.md) | Returns the next ICoreFragment objects in the knowledge, if they are available. |
| [ICoreFragmentInspector::Reset](..\winsync\nf-winsync-icorefragmentinspector-reset.md) | Resets the enumerator to the beginning of the knowledge. |
| [IDataRetrieverCallback::LoadChangeDataComplete](..\winsync\nf-winsync-idataretrievercallback-loadchangedatacomplete.md) | Indicates that IAsynchronousDataRetriever |
| [IDataRetrieverCallback::LoadChangeDataError](..\winsync\nf-winsync-idataretrievercallback-loadchangedataerror.md) | Indicates that an IAsynchronousDataRetriever method failed. |
| [IEnumChangeUnitExceptions::Clone](..\winsync\nf-winsync-ienumchangeunitexceptions-clone.md) | Clones the enumerator and returns a new enumerator that is in the same state as the current one. |
| [IEnumChangeUnitExceptions::Next](..\winsync\nf-winsync-ienumchangeunitexceptions-next.md) | Returns the next elements in the change unit exception set, if they are available. |
| [IEnumChangeUnitExceptions::Reset](..\winsync\nf-winsync-ienumchangeunitexceptions-reset.md) | Resets the enumerator to the beginning of the change unit exception set. |
| [IEnumChangeUnitExceptions::Skip](..\winsync\nf-winsync-ienumchangeunitexceptions-skip.md) | Skips the specified number of change unit exceptions. |
| [IEnumClockVector::Clone](..\winsync\nf-winsync-ienumclockvector-clone.md) | Clones the enumerator and returns a new enumerator that is in the same state as the current one. |
| [IEnumClockVector::Next](..\winsync\nf-winsync-ienumclockvector-next.md) | Returns the next elements in the clock vector, if they are available. |
| [IEnumClockVector::Reset](..\winsync\nf-winsync-ienumclockvector-reset.md) | Resets the enumerator to the beginning of the clock vector. |
| [IEnumClockVector::Skip](..\winsync\nf-winsync-ienumclockvector-skip.md) | Skips the specified number of clock vector elements. |
| [IEnumFeedClockVector::Clone](..\winsync\nf-winsync-ienumfeedclockvector-clone.md) | Clones the enumerator and returns a new enumerator that is in the same state as the current one. |
| [IEnumFeedClockVector::Next](..\winsync\nf-winsync-ienumfeedclockvector-next.md) | Returns the next elements in the clock vector, if available. |
| [IEnumFeedClockVector::Reset](..\winsync\nf-winsync-ienumfeedclockvector-reset.md) | Resets the enumerator to the beginning of the clock vector. |
| [IEnumFeedClockVector::Skip](..\winsync\nf-winsync-ienumfeedclockvector-skip.md) | Skips the specified number of clock vector elements. |
| [IEnumRangeExceptions::Clone](..\winsync\nf-winsync-ienumrangeexceptions-clone.md) | Clones the enumerator and returns a new enumerator that is in the same state as the current one. |
| [IEnumRangeExceptions::Next](..\winsync\nf-winsync-ienumrangeexceptions-next.md) | Returns the next elements in the change unit exception set, if they are available. |
| [IEnumRangeExceptions::Reset](..\winsync\nf-winsync-ienumrangeexceptions-reset.md) | Resets the enumerator to the beginning of the range exception set. |
| [IEnumRangeExceptions::Skip](..\winsync\nf-winsync-ienumrangeexceptions-skip.md) | Skips the specified number of range exceptions. |
| [IEnumSingleItemExceptions::Clone](..\winsync\nf-winsync-ienumsingleitemexceptions-clone.md) | Clones the enumerator and returns a new enumerator that is in the same state as the current one. |
| [IEnumSingleItemExceptions::Next](..\winsync\nf-winsync-ienumsingleitemexceptions-next.md) | Returns the next elements in the single-item exception set, if they are available. |
| [IEnumSingleItemExceptions::Reset](..\winsync\nf-winsync-ienumsingleitemexceptions-reset.md) | Resets the enumerator to the beginning of the single-item exception set. |
| [IEnumSingleItemExceptions::Skip](..\winsync\nf-winsync-ienumsingleitemexceptions-skip.md) | Skips the specified number of single-item exceptions. |
| [IEnumSyncChangeUnits::Clone](..\winsync\nf-winsync-ienumsyncchangeunits-clone.md) | This method is not implemented. |
| [IEnumSyncChangeUnits::Next](..\winsync\nf-winsync-ienumsyncchangeunits-next.md) | Returns the next change unit. |
| [IEnumSyncChangeUnits::Reset](..\winsync\nf-winsync-ienumsyncchangeunits-reset.md) | Resets the enumerator to the beginning of the list. |
| [IEnumSyncChangeUnits::Skip](..\winsync\nf-winsync-ienumsyncchangeunits-skip.md) | This method is not implemented. |
| [IEnumSyncChanges::Clone](..\winsync\nf-winsync-ienumsyncchanges-clone.md) | This method is not implemented. |
| [IEnumSyncChanges::Next](..\winsync\nf-winsync-ienumsyncchanges-next.md) | Returns the next item change. |
| [IEnumSyncChanges::Reset](..\winsync\nf-winsync-ienumsyncchanges-reset.md) | Resets the enumerator to the beginning of the list. |
| [IEnumSyncChanges::Skip](..\winsync\nf-winsync-ienumsyncchanges-skip.md) | This method is not implemented. |
| [IEnumSyncProviderConfigUIInfos::Clone](..\syncregistration\nf-syncregistration-ienumsyncproviderconfiguiinfos-clone.md) | Clones the enumerator and returns a new enumerator that is in the same state as the current one. |
| [IEnumSyncProviderConfigUIInfos::Next](..\syncregistration\nf-syncregistration-ienumsyncproviderconfiguiinfos-next.md) | Returns the next ISyncProviderConfigUIInfo object. |
| [IEnumSyncProviderConfigUIInfos::Reset](..\syncregistration\nf-syncregistration-ienumsyncproviderconfiguiinfos-reset.md) | Resets the enumerator to the beginning of the collection of ISyncProviderConfigUIInfo objects. |
| [IEnumSyncProviderConfigUIInfos::Skip](..\syncregistration\nf-syncregistration-ienumsyncproviderconfiguiinfos-skip.md) | Skips the specified number of ISyncProviderConfigUIInfo objects. |
| [IEnumSyncProviderInfos::Clone](..\syncregistration\nf-syncregistration-ienumsyncproviderinfos-clone.md) | Clones the enumerator and returns a new enumerator that is in the same state as the current one. |
| [IEnumSyncProviderInfos::Next](..\syncregistration\nf-syncregistration-ienumsyncproviderinfos-next.md) | Returns the next ISyncProviderInfo object. |
| [IEnumSyncProviderInfos::Reset](..\syncregistration\nf-syncregistration-ienumsyncproviderinfos-reset.md) | Resets the enumerator to the beginning of the ISyncProviderInfo set. |
| [IEnumSyncProviderInfos::Skip](..\syncregistration\nf-syncregistration-ienumsyncproviderinfos-skip.md) | Skips the specified number of ISyncProviderInfo objects. |
| [IFeedClockVector::GetUpdateCount](..\winsync\nf-winsync-ifeedclockvector-getupdatecount.md) | Gets the number of updates that have been made to the FeedSync item. |
| [IFeedClockVector::IsNoConflictsSpecified](..\winsync\nf-winsync-ifeedclockvector-isnoconflictsspecified.md) | Gets a value that indicates whether conflicts are preserved for the FeedSync item. |
| [IFeedClockVectorElement::GetFlags](..\winsync\nf-winsync-ifeedclockvectorelement-getflags.md) | Gets flags that specify additional information about the clock vector element. |
| [IFeedClockVectorElement::GetSyncTime](..\winsync\nf-winsync-ifeedclockvectorelement-getsynctime.md) | Gets a SYNC_TIME value that corresponds to the when value for the item. |
| [IFilterRequestCallback::RequestFilter](..\winsync\nf-winsync-ifilterrequestcallback-requestfilter.md) | Requests that the filter that is specified by the destination provider be used by the source provider during change enumeration. |
| [IForgottenKnowledge::ForgetToVersion](..\winsync\nf-winsync-iforgottenknowledge-forgettoversion.md) | Updates the forgotten knowledge to reflect that all versions that are less than or equal to the specified version might have been forgotten, and that corresponding tombstones might have been deleted. |
| [IKnowledgeSyncProvider::BeginSession](..\winsync\nf-winsync-iknowledgesyncprovider-beginsession.md) | Notifies the provider that it is joining a synchronization session. |
| [IKnowledgeSyncProvider::EndSession](..\winsync\nf-winsync-iknowledgesyncprovider-endsession.md) | Notifies the provider that a synchronization session to which it was enlisted has finished. |
| [IKnowledgeSyncProvider::GetChangeBatch](..\winsync\nf-winsync-iknowledgesyncprovider-getchangebatch.md) | Gets a change batch that contains item metadata for items that are not contained in the specified knowledge from the destination provider. |
| [IKnowledgeSyncProvider::GetFullEnumerationChangeBatch](..\winsync\nf-winsync-iknowledgesyncprovider-getfullenumerationchangebatch.md) | Gets a change batch that contains item metadata for items that have IDs greater than the specified lower bound, as part of a full enumeration. |
| [IKnowledgeSyncProvider::GetSyncBatchParameters](..\winsync\nf-winsync-iknowledgesyncprovider-getsyncbatchparameters.md) | Gets the requested number of item changes that will be included in change batches, and the current knowledge for the synchronization scope. |
| [IKnowledgeSyncProvider::ProcessChangeBatch](..\winsync\nf-winsync-iknowledgesyncprovider-processchangebatch.md) | Processes a set of changes by detecting conflicts and applying changes to the item store. |
| [IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch](..\winsync\nf-winsync-iknowledgesyncprovider-processfullenumerationchangebatch.md) | Processes a set of changes for a full enumeration by applying changes to the item store. |
| [ILoadChangeContext::GetSyncChange](..\winsync\nf-winsync-iloadchangecontext-getsyncchange.md) | Gets the change item for which the change data should be retrieved from the item store. |
| [ILoadChangeContext::SetRecoverableErrorOnChangeUnit](..\winsync\nf-winsync-iloadchangecontext-setrecoverableerroronchangeunit.md) | Indicates that a recoverable error occurred when data for the specified change unit was loaded from the item store. |
| [ILoadChangeContext::SetRecoverableErrorOnChange](..\winsync\nf-winsync-iloadchangecontext-setrecoverableerroronchange.md) | Indicates a recoverable error on this change has occurred. |
| [IProviderConverter::Initialize](..\winsync\nf-winsync-iproviderconverter-initialize.md) | When implemented by a derived class, initializes the IProviderConverter object with the ISyncProvider object to be converted to IKnowledgeSyncProvider. |
| [IRangeException::GetClockVector](..\winsync\nf-winsync-irangeexception-getclockvector.md) | Gets the clock vector that is associated with this exception. |
| [IRangeException::GetClosedRangeEnd](..\winsync\nf-winsync-irangeexception-getclosedrangeend.md) | Gets the upper bound of the range of item IDs to exclude. |
| [IRangeException::GetClosedRangeStart](..\winsync\nf-winsync-irangeexception-getclosedrangestart.md) | Gets the lower bound of the range of item IDs to exclude. |
| [IRecoverableError::GetChangeWithRecoverableError](..\winsync\nf-winsync-irecoverableerror-getchangewithrecoverableerror.md) | Gets the item change that caused the error. |
| [IRecoverableError::GetProvider](..\winsync\nf-winsync-irecoverableerror-getprovider.md) | Gets the role of the provider that skipped the item change. |
| [IRecoverableError::GetRecoverableErrorDataForChangeUnit](..\winsync\nf-winsync-irecoverableerror-getrecoverableerrordataforchangeunit.md) | Gets additional data about the recoverable error for a specified change unit. |
| [IRecoverableError::GetRecoverableErrorDataForChange](..\winsync\nf-winsync-irecoverableerror-getrecoverableerrordataforchange.md) | Gets additional data about the recoverable error. |
| [IRecoverableError::GetStage](..\winsync\nf-winsync-irecoverableerror-getstage.md) | Gets the stage in the synchronization session when the error occurred. |
| [IRecoverableErrorData::GetErrorDescription](..\winsync\nf-winsync-irecoverableerrordata-geterrordescription.md) | Gets the description of the error. |
| [IRecoverableErrorData::GetItemDisplayName](..\winsync\nf-winsync-irecoverableerrordata-getitemdisplayname.md) | Gets the display name of the item that caused the error. |
| [IRecoverableErrorData::Initialize](..\winsync\nf-winsync-irecoverableerrordata-initialize.md) | Initializes the object by using the specified display name of the item that caused the error and a description of the error. |
| [IRegisteredSyncProvider::GetInstanceId](..\syncregistration\nf-syncregistration-iregisteredsyncprovider-getinstanceid.md) | Returns the synchronization provider's instance ID. |
| [IRegisteredSyncProvider::Init](..\syncregistration\nf-syncregistration-iregisteredsyncprovider-init.md) | Initializes the synchronization provider before it is ready for a synchronization session. |
| [IRegisteredSyncProvider::Reset](..\syncregistration\nf-syncregistration-iregisteredsyncprovider-reset.md) | Resets a synchronization provider so that it looks like a new replica in the next synchronization session. |
| [IReplicaKeyMap::LookupReplicaId](..\winsync\nf-winsync-ireplicakeymap-lookupreplicaid.md) | Gets the replica ID that corresponds to the specified replica key. |
| [IReplicaKeyMap::LookupReplicaKey](..\winsync\nf-winsync-ireplicakeymap-lookupreplicakey.md) | Gets the replica key that corresponds to the specified replica ID. |
| [IReplicaKeyMap::Serialize](..\winsync\nf-winsync-ireplicakeymap-serialize.md) | Serializes the replica key map data to a byte array. |
| [IRequestFilteredSync::SpecifyFilter](..\winsync\nf-winsync-irequestfilteredsync-specifyfilter.md) | When implemented by a derived class, negotiates which filter is used by the source provider during change enumeration. |
| [ISingleItemException::GetClockVector](..\winsync\nf-winsync-isingleitemexception-getclockvector.md) | Gets the clock vector that is associated with the item exception. |
| [ISingleItemException::GetItemId](..\winsync\nf-winsync-isingleitemexception-getitemid.md) | Gets the ID of the item that is specified in the exception. |
| [ISupportFilteredSync::AddFilter](..\winsync\nf-winsync-isupportfilteredsync-addfilter.md) | Sets the filter that is used for change enumeration by the source provider, when implemented by a derived class. |
| [ISupportLastWriteTime::GetChangeUnitChangeTime](..\winsync\nf-winsync-isupportlastwritetime-getchangeunitchangetime.md) | Gets the date and time when the specified change unit was last changed. |
| [ISupportLastWriteTime::GetItemChangeTime](..\winsync\nf-winsync-isupportlastwritetime-getitemchangetime.md) | Gets the date and time when the specified item was last changed. |
| [ISyncCallback2::OnChangeApplied](..\winsync\nf-winsync-isynccallback2-onchangeapplied.md) | Occurs after a change is successfully applied. |
| [ISyncCallback2::OnChangeFailed](..\winsync\nf-winsync-isynccallback2-onchangefailed.md) | Occurs after a change fails to apply. |
| [ISyncCallback::OnChange](..\winsync\nf-winsync-isynccallback-onchange.md) | Occurs before a change is applied. |
| [ISyncCallback::OnConflict](..\winsync\nf-winsync-isynccallback-onconflict.md) | Occurs when a conflict is detected when the concurrency conflict resolution policy is set to CRP_NONE. |
| [ISyncCallback::OnFullEnumerationNeeded](..\winsync\nf-winsync-isynccallback-onfullenumerationneeded.md) | Occurs when the forgotten knowledge from the source provider is not contained in the current knowledge of the destination provider. |
| [ISyncCallback::OnProgress](..\winsync\nf-winsync-isynccallback-onprogress.md) | Occurs periodically during the synchronization session to report progress. |
| [ISyncCallback::OnRecoverableError](..\winsync\nf-winsync-isynccallback-onrecoverableerror.md) | Occurs when a synchronization provider sets a recoverable error when it is loading or saving an item. |
| [ISyncChange::GetChangeUnits](..\winsync\nf-winsync-isyncchange-getchangeunits.md) | Gets an object that can enumerate change units that are contained in this change. |
| [ISyncChange::GetChangeVersion](..\winsync\nf-winsync-isyncchange-getchangeversion.md) | Gets the version that is associated with this change. |
| [ISyncChange::GetCreationVersion](..\winsync\nf-winsync-isyncchange-getcreationversion.md) | Gets the creation version of the changed item. |
| [ISyncChange::GetFlags](..\winsync\nf-winsync-isyncchange-getflags.md) | Gets flags that are associated with this change. |
| [ISyncChange::GetLearnedKnowledge](..\winsync\nf-winsync-isyncchange-getlearnedknowledge.md) | Gets the knowledge that a replica will learn when this change is applied to its item store. |
| [ISyncChange::GetMadeWithKnowledge](..\winsync\nf-winsync-isyncchange-getmadewithknowledge.md) | Gets the made-with knowledge for this change. |
| [ISyncChange::GetOwnerReplicaId](..\winsync\nf-winsync-isyncchange-getownerreplicaid.md) | Gets the ID of the replica that originated this change. |
| [ISyncChange::GetRootItemId](..\winsync\nf-winsync-isyncchange-getrootitemid.md) | Gets the ID of the changed item. |
| [ISyncChange::GetWorkEstimate](..\winsync\nf-winsync-isyncchange-getworkestimate.md) | Gets the work estimate for this change. |
| [ISyncChange::SetWorkEstimate](..\winsync\nf-winsync-isyncchange-setworkestimate.md) | Sets the work estimate for this change. |
| [ISyncChangeBatch::AddLoggedConflict](..\winsync\nf-winsync-isyncchangebatch-addloggedconflict.md) | Adds metadata that represents a conflict to the change batch. |
| [ISyncChangeBatch::BeginUnorderedGroup](..\winsync\nf-winsync-isyncchangebatch-beginunorderedgroup.md) | Opens an unordered group in the change batch. Item changes in this group can be in any order. |
| [ISyncChangeBatch::EndUnorderedGroup](..\winsync\nf-winsync-isyncchangebatch-endunorderedgroup.md) | Closes a previously opened unordered group in the change batch. |
| [ISyncChangeBatchAdvanced::ConvertFullEnumerationChangeBatchToRegularChangeBatch](..\winsync\nf-winsync-isyncchangebatchadvanced-convertfullenumerationchangebatchtoregularchangebatch.md) | Converts an ISyncFullEnumerationChangeBatch object to an ISyncChangeBatch object. |
| [ISyncChangeBatchAdvanced::GetBatchLevelKnowledgeShouldBeApplied](..\winsync\nf-winsync-isyncchangebatchadvanced-getbatchlevelknowledgeshouldbeapplied.md) | Gets a value that indicates whether the learned knowledge for the batch must be saved after the batch is applied to the destination replica. |
| [ISyncChangeBatchAdvanced::GetFilterInfo](..\winsync\nf-winsync-isyncchangebatchadvanced-getfilterinfo.md) | Gets the ISyncFilterInfo that was specified when the change batch was created. |
| [ISyncChangeBatchAdvanced::GetUpperBoundItemId](..\winsync\nf-winsync-isyncchangebatchadvanced-getupperbounditemid.md) | Gets the highest item ID that is represented in the knowledge of any group in the change batch. |
| [ISyncChangeBatchBase2::SerializeWithOptions](..\winsync\nf-winsync-isyncchangebatchbase2-serializewithoptions.md) | Serializes the change batch object data to a byte array, based on the specified version and serialization options. |
| [ISyncChangeBatchBase::AddItemMetadataToGroup](..\winsync\nf-winsync-isyncchangebatchbase-additemmetadatatogroup.md) | Adds a specified item change to the group that is currently open. |
| [ISyncChangeBatchBase::BeginOrderedGroup](..\winsync\nf-winsync-isyncchangebatchbase-beginorderedgroup.md) | Opens an ordered group in the change batch. This group is ordered by item ID. |
| [ISyncChangeBatchBase::EndOrderedGroup](..\winsync\nf-winsync-isyncchangebatchbase-endorderedgroup.md) | Closes a previously opened ordered group in the change batch. |
| [ISyncChangeBatchBase::GetChangeEnumerator](..\winsync\nf-winsync-isyncchangebatchbase-getchangeenumerator.md) | Gets an IEnumSyncChanges object that enumerates the item changes in this change batch. |
| [ISyncChangeBatchBase::GetIsLastBatch](..\winsync\nf-winsync-isyncchangebatchbase-getislastbatch.md) | Gets a flag that indicates whether the changes in this change batch are the last batch of a synchronization session. |
| [ISyncChangeBatchBase::GetLearnedKnowledge](..\winsync\nf-winsync-isyncchangebatchbase-getlearnedknowledge.md) | Gets the knowledge that the destination replica learns when the destination provider applies all the changes in this change batch. |
| [ISyncChangeBatchBase::GetPrerequisiteKnowledge](..\winsync\nf-winsync-isyncchangebatchbase-getprerequisiteknowledge.md) | Gets the minimum knowledge that a destination provider is required to have to process this change batch. |
| [ISyncChangeBatchBase::GetRemainingWorkEstimateForSession](..\winsync\nf-winsync-isyncchangebatchbase-getremainingworkestimateforsession.md) | Gets the estimate of the remaining work for the session. |
| [ISyncChangeBatchBase::GetSourceForgottenKnowledge](..\winsync\nf-winsync-isyncchangebatchbase-getsourceforgottenknowledge.md) | Gets the forgotten knowledge of the source replica. |
| [ISyncChangeBatchBase::GetWorkEstimateForBatch](..\winsync\nf-winsync-isyncchangebatchbase-getworkestimateforbatch.md) | Gets the work estimate for the batch. |
| [ISyncChangeBatchBase::Serialize](..\winsync\nf-winsync-isyncchangebatchbase-serialize.md) | Serializes the change batch to an array of bytes. |
| [ISyncChangeBatchBase::SetLastBatch](..\winsync\nf-winsync-isyncchangebatchbase-setlastbatch.md) | Sets a flag that indicates there are no more changes to be enumerated in the synchronization session. |
| [ISyncChangeBatchBase::SetRemainingWorkEstimateForSession](..\winsync\nf-winsync-isyncchangebatchbase-setremainingworkestimateforsession.md) | Sets the estimate of the remaining work for the session. |
| [ISyncChangeBatchBase::SetWorkEstimateForBatch](..\winsync\nf-winsync-isyncchangebatchbase-setworkestimateforbatch.md) | Sets the work estimate for the batch. |
| [ISyncChangeBatchWithPrerequisite::GetLearnedForgottenKnowledge](..\winsync\nf-winsync-isyncchangebatchwithprerequisite-getlearnedforgottenknowledge.md) | Gets the forgotten knowledge that the destination replica learns when the destination provider applies all the changes in this change batch during recovery synchronization. |
| [ISyncChangeBatchWithPrerequisite::GetLearnedKnowledgeWithPrerequisite](..\winsync\nf-winsync-isyncchangebatchwithprerequisite-getlearnedknowledgewithprerequisite.md) | Gets the knowledge that the destination replica learns when the destination provider applies all the changes in this change batch, based on the prerequisite knowledge of the change batch. |
| [ISyncChangeBatchWithPrerequisite::SetPrerequisiteKnowledge](..\winsync\nf-winsync-isyncchangebatchwithprerequisite-setprerequisiteknowledge.md) | Sets the minimum knowledge that a destination provider is required to have to process this change batch. |
| [ISyncChangeBuilder::AddChangeUnitMetadata](..\winsync\nf-winsync-isyncchangebuilder-addchangeunitmetadata.md) | Adds change unit metadata to an item change. |
| [ISyncChangeUnit::GetChangeUnitId](..\winsync\nf-winsync-isyncchangeunit-getchangeunitid.md) | Retrieves the ID for this change unit. |
| [ISyncChangeUnit::GetChangeUnitVersion](..\winsync\nf-winsync-isyncchangeunit-getchangeunitversion.md) | Gets the version for the change unit change. |
| [ISyncChangeUnit::GetItemChange](..\winsync\nf-winsync-isyncchangeunit-getitemchange.md) | Gets the item change that contains this change unit change. |
| [ISyncChangeWithPrerequisite::GetLearnedKnowledgeWithPrerequisite](..\winsync\nf-winsync-isyncchangewithprerequisite-getlearnedknowledgewithprerequisite.md) | Gets the knowledge that the destination replica learns when the destination provider applies this change, based on the prerequisite knowledge that is associated with the change. |
| [ISyncChangeWithPrerequisite::GetPrerequisiteKnowledge](..\winsync\nf-winsync-isyncchangewithprerequisite-getprerequisiteknowledge.md) | Gets the minimum knowledge that a destination provider is required to have to process this change. |
| [ISyncFilterInfo2::GetFlags](..\winsync\nf-winsync-isyncfilterinfo2-getflags.md) | Gets the flags that specify additional information about the filter information object. |
| [ISyncFilterInfo::Serialize](..\winsync\nf-winsync-isyncfilterinfo-serialize.md) | Serializes the filter data to an array of bytes. |
| [ISyncFullEnumerationChange::GetLearnedForgottenKnowledge](..\winsync\nf-winsync-isyncfullenumerationchange-getlearnedforgottenknowledge.md) | Gets the forgotten knowledge that the destination replica learns when the destination provider applies this change during recovery synchronization. |
| [ISyncFullEnumerationChange::GetLearnedKnowledgeAfterRecoveryComplete](..\winsync\nf-winsync-isyncfullenumerationchange-getlearnedknowledgeafterrecoverycomplete.md) | Gets the knowledge the destination replica will learn after it applies the changes in the full enumeration. |
| [ISyncFullEnumerationChangeBatch::GetClosedLowerBoundItemId](..\winsync\nf-winsync-isyncfullenumerationchangebatch-getclosedlowerbounditemid.md) | Gets the closed lower bound on item IDs that require destination versions. |
| [ISyncFullEnumerationChangeBatch::GetClosedUpperBoundItemId](..\winsync\nf-winsync-isyncfullenumerationchangebatch-getclosedupperbounditemid.md) | Gets the closed upper bound on item IDs that require destination versions. |
| [ISyncFullEnumerationChangeBatch::GetLearnedKnowledgeAfterRecoveryComplete](..\winsync\nf-winsync-isyncfullenumerationchangebatch-getlearnedknowledgeafterrecoverycomplete.md) | Gets the knowledge the destination replica will learn after it applies all the changes in the recovery synchronization. |
| [ISyncKnowledge2::CompareToKnowledgeCookie](..\winsync\nf-winsync-isyncknowledge2-comparetoknowledgecookie.md) | Performs a fast comparison between the specified knowledge cookie and this knowledge object. |
| [ISyncKnowledge2::Complement](..\winsync\nf-winsync-isyncknowledge2-complement.md) | Returns the knowledge that is contained in this object but that is not contained in the specified knowledge. |
| [ISyncKnowledge2::ContainsKnowledgeForChangeUnit](..\winsync\nf-winsync-isyncknowledge2-containsknowledgeforchangeunit.md) | Indicates whether the specified knowledge of the specified change unit is known by this knowledge. |
| [ISyncKnowledge2::ContainsKnowledgeForItem](..\winsync\nf-winsync-isyncknowledge2-containsknowledgeforitem.md) | Indicates whether the specified knowledge of the specified item is known by this knowledge. |
| [ISyncKnowledge2::GetIdParameters](..\winsync\nf-winsync-isyncknowledge2-getidparameters.md) | Gets the ID format schema of the provider. |
| [ISyncKnowledge2::GetInspector](..\winsync\nf-winsync-isyncknowledge2-getinspector.md) | Returns an object that can be used to retrieve the contents of the knowledge object. |
| [ISyncKnowledge2::GetKnowledgeCookie](..\winsync\nf-winsync-isyncknowledge2-getknowledgecookie.md) | Gets a lightweight, read-only representation of this knowledge object that can be used for fast comparisons. |
| [ISyncKnowledge2::GetLowestUncontainedId](..\winsync\nf-winsync-isyncknowledge2-getlowestuncontainedid.md) | Returns the lowest item ID that is not contained in this knowledge and that is contained in the specified knowledge. |
| [ISyncKnowledge2::GetMinimumSupportedVersion](..\winsync\nf-winsync-isyncknowledge2-getminimumsupportedversion.md) | Gets the minimum supported version of Microsoft Sync Framework components that can be used with this object. |
| [ISyncKnowledge2::GetStatistics](..\winsync\nf-winsync-isyncknowledge2-getstatistics.md) | Gets the specified statistic data that is contained in this object. |
| [ISyncKnowledge2::IntersectsWithKnowledge](..\winsync\nf-winsync-isyncknowledge2-intersectswithknowledge.md) | Indicates whether the specified knowledge intersects with this knowledge. |
| [ISyncKnowledge2::ProjectOntoColumnSet](..\winsync\nf-winsync-isyncknowledge2-projectontocolumnset.md) | Returns the knowledge for the specified set of change units for all the items that are contained in this object. |
| [ISyncKnowledge2::ProjectOntoKnowledgeWithPrerequisite](..\winsync\nf-winsync-isyncknowledge2-projectontoknowledgewithprerequisite.md) | Returns knowledge about the knowledge fragments that are specified by the template knowledge, when the template knowledge contains the prerequisite knowledge for the specified fragments. |
| [ISyncKnowledge2::SerializeWithOptions](..\winsync\nf-winsync-isyncknowledge2-serializewithoptions.md) | Serializes the knowledge object data to a byte array based on the specified version and serialization options. |
| [ISyncKnowledge::Clone](..\winsync\nf-winsync-isyncknowledge-clone.md) | Creates a new instance of this object, and copies the data from this object to the new object. |
| [ISyncKnowledge::ContainsChangeUnit](..\winsync\nf-winsync-isyncknowledge-containschangeunit.md) | Indicates whether the specified change unit change is known by this knowledge. |
| [ISyncKnowledge::ContainsChange](..\winsync\nf-winsync-isyncknowledge-containschange.md) | Indicates whether the specified item change is known by this knowledge. |
| [ISyncKnowledge::ContainsKnowledge](..\winsync\nf-winsync-isyncknowledge-containsknowledge.md) | Indicates whether the specified knowledge is known by this knowledge. |
| [ISyncKnowledge::ConvertVersion](..\winsync\nf-winsync-isyncknowledge-convertversion.md) | Converts a version from another replica into one that is compatible with the replica that owns this knowledge. |
| [ISyncKnowledge::ExcludeChangeUnit](..\winsync\nf-winsync-isyncknowledge-excludechangeunit.md) | Removes knowledge about the specified change unit from the knowledge. |
| [ISyncKnowledge::ExcludeItem](..\winsync\nf-winsync-isyncknowledge-excludeitem.md) | Removes knowledge about the specified item from the knowledge. |
| [ISyncKnowledge::FindClockVectorForChangeUnit](..\winsync\nf-winsync-isyncknowledge-findclockvectorforchangeunit.md) | Gets the clock vector that is associated with the specified change unit ID. |
| [ISyncKnowledge::FindClockVectorForItem](..\winsync\nf-winsync-isyncknowledge-findclockvectorforitem.md) | Gets the clock vector that is associated with the specified item ID. |
| [ISyncKnowledge::FindMinTickCountForReplica](..\winsync\nf-winsync-isyncknowledge-findmintickcountforreplica.md) | Finds the minimum tick count in the knowledge for the specified replica. |
| [ISyncKnowledge::GetChangeUnitExceptions](..\winsync\nf-winsync-isyncknowledge-getchangeunitexceptions.md) | Gets an object that can enumerate the IChangeUnitException objects that are stored in the knowledge. |
| [ISyncKnowledge::GetOwnerReplicaId](..\winsync\nf-winsync-isyncknowledge-getownerreplicaid.md) | Gets the ID of the replica that owns this knowledge. |
| [ISyncKnowledge::GetRangeExceptions](..\winsync\nf-winsync-isyncknowledge-getrangeexceptions.md) | Gets an object that can enumerate the IRangeException objects that are stored in the knowledge. |
| [ISyncKnowledge::GetReplicaKeyMap](..\winsync\nf-winsync-isyncknowledge-getreplicakeymap.md) | Gets the IReplicaKeyMap object that is associated with this knowledge. |
| [ISyncKnowledge::GetScopeVector](..\winsync\nf-winsync-isyncknowledge-getscopevector.md) | Gets the clock vector that defines the changes that are contained in the knowledge. |
| [ISyncKnowledge::GetSingleItemExceptions](..\winsync\nf-winsync-isyncknowledge-getsingleitemexceptions.md) | Gets an object that can enumerate the ISingleItemException objects that are stored in the knowledge. |
| [ISyncKnowledge::GetVersion](..\winsync\nf-winsync-isyncknowledge-getversion.md) | Gets the version of this knowledge structure. |
| [ISyncKnowledge::MapRemoteToLocal](..\winsync\nf-winsync-isyncknowledge-mapremotetolocal.md) | Converts a knowledge object from another replica into one that is compatible with the replica that owns this knowledge. |
| [ISyncKnowledge::ProjectOntoChangeUnit](..\winsync\nf-winsync-isyncknowledge-projectontochangeunit.md) | Gets the knowledge for the specified change unit. |
| [ISyncKnowledge::ProjectOntoItem](..\winsync\nf-winsync-isyncknowledge-projectontoitem.md) | Gets the knowledge for the specified item. |
| [ISyncKnowledge::ProjectOntoRange](..\winsync\nf-winsync-isyncknowledge-projectontorange.md) | Gets the knowledge for the specified range of item IDs. |
| [ISyncKnowledge::Serialize](..\winsync\nf-winsync-isyncknowledge-serialize.md) | Serializes the knowledge object data to a byte array. |
| [ISyncKnowledge::SetLocalTickCount](..\winsync\nf-winsync-isyncknowledge-setlocaltickcount.md) | Sets the tick count for the replica that owns this knowledge. |
| [ISyncKnowledge::Union](..\winsync\nf-winsync-isyncknowledge-union.md) | Combines the specified knowledge with the current knowledge. |
| [ISyncProvider::GetIdParameters](..\winsync\nf-winsync-isyncprovider-getidparameters.md) | Gets the ID format schema of the provider. |
| [ISyncProviderConfigUI::CreateAndRegisterNewSyncProvider](..\syncregistration\nf-syncregistration-isyncproviderconfigui-createandregisternewsyncprovider.md) | Creates and registers a new synchronization provider. |
| [ISyncProviderConfigUI::GetRegisteredProperties](..\syncregistration\nf-syncregistration-isyncproviderconfigui-getregisteredproperties.md) | Obtains configuration UI properties for reading and writing. |
| [ISyncProviderConfigUI::Init](..\syncregistration\nf-syncregistration-isyncproviderconfigui-init.md) | Initializes the configuration UI for a synchronization provider. |
| [ISyncProviderConfigUI::ModifySyncProvider](..\syncregistration\nf-syncregistration-isyncproviderconfigui-modifysyncprovider.md) | Updates the ISyncProviderInfo of the synchronization provider that is configured by this ISyncProviderConfigUI. |
| [ISyncProviderConfigUIInfo::GetSyncProviderConfigUI](..\syncregistration\nf-syncregistration-isyncproviderconfiguiinfo-getsyncproviderconfigui.md) | Creates an instance of a synchronization provider configuration UI. |
| [ISyncProviderInfo::GetSyncProvider](..\syncregistration\nf-syncregistration-isyncproviderinfo-getsyncprovider.md) | Creates an instance of the synchronization provider. |
| [ISyncProviderRegistration::CreateSyncProviderConfigUIRegistrationInstance](..\syncregistration\nf-syncregistration-isyncproviderregistration-createsyncproviderconfiguiregistrationinstance.md) | Creates an in-memory instance of a synchronization provider configuration UI. |
| [ISyncProviderRegistration::CreateSyncProviderRegistrationInstance](..\syncregistration\nf-syncregistration-isyncproviderregistration-createsyncproviderregistrationinstance.md) | Creates an in-memory instance of a synchronization provider. |
| [ISyncProviderRegistration::EnumerateSyncProviderConfigUIs](..\syncregistration\nf-syncregistration-isyncproviderregistration-enumeratesyncproviderconfiguis.md) | Returns an IEnumSyncProviderConfigUIInfos enumeration interface that enumerates all registered ISyncProviderConfigUIInfo objects for the specified criteria. |
| [ISyncProviderRegistration::EnumerateSyncProviders](..\syncregistration\nf-syncregistration-isyncproviderregistration-enumeratesyncproviders.md) | Returns an IEnumSyncProviderInfos enumeration interface that enumerates all registered ISyncProviderInfo objects for the specified criteria. |
| [ISyncProviderRegistration::GetChange](..\syncregistration\nf-syncregistration-isyncproviderregistration-getchange.md) | Gets an ISyncRegistrationChange object that represents a new registration event. |
| [ISyncProviderRegistration::GetSyncProviderConfigUIFromInstanceId](..\syncregistration\nf-syncregistration-isyncproviderregistration-getsyncproviderconfiguifrominstanceid.md) | Returns an initialized and instantiated ISyncProviderConfigUI object for the given unique instance ID. |
| [ISyncProviderRegistration::GetSyncProviderConfigUIInfo](..\syncregistration\nf-syncregistration-isyncproviderregistration-getsyncproviderconfiguiinfo.md) | Returns an ISyncProviderConfigUIInfo object for the given unique instance ID. |
| [ISyncProviderRegistration::GetSyncProviderConfigUIInfoforProvider](..\syncregistration\nf-syncregistration-isyncproviderregistration-getsyncproviderconfiguiinfoforprovider.md) | Returns an ISyncProviderConfigUIInfo object for the specified synchronization provider instance ID. |
| [ISyncProviderRegistration::GetSyncProviderFromInstanceId](..\syncregistration\nf-syncregistration-isyncproviderregistration-getsyncproviderfrominstanceid.md) | Returns an initialized and instantiated IRegisteredSyncProvider object for the specific unique instance ID. |
| [ISyncProviderRegistration::GetSyncProviderInfo](..\syncregistration\nf-syncregistration-isyncproviderregistration-getsyncproviderinfo.md) | Returns an ISyncProviderInfo object for the specific synchronization provider instance ID. |
| [ISyncProviderRegistration::GetSyncProviderState](..\syncregistration\nf-syncregistration-isyncproviderregistration-getsyncproviderstate.md) | Returns the state of the specified synchronization provider. |
| [ISyncProviderRegistration::RegisterForEvent](..\syncregistration\nf-syncregistration-isyncproviderregistration-registerforevent.md) | Registers the user to receive notification of the arrival of new registration events that oocur when changes are made to the registration store. |
| [ISyncProviderRegistration::RevokeEvent](..\syncregistration\nf-syncregistration-isyncproviderregistration-revokeevent.md) | Unregisters the user from the notification of the arrival of new registration events. |
| [ISyncProviderRegistration::SetSyncProviderState](..\syncregistration\nf-syncregistration-isyncproviderregistration-setsyncproviderstate.md) | Sets the state of the specified synchronization provider. |
| [ISyncProviderRegistration::UnregisterSyncProviderConfigUI](..\syncregistration\nf-syncregistration-isyncproviderregistration-unregistersyncproviderconfigui.md) | Unregisters and removes the specified synchronization provider configuration UI from the registration store. |
| [ISyncProviderRegistration::UnregisterSyncProvider](..\syncregistration\nf-syncregistration-isyncproviderregistration-unregistersyncprovider.md) | Unregisters and removes the specified synchronization provider from the registration store. |
| [ISyncRegistrationChange::GetEvent](..\syncregistration\nf-syncregistration-isyncregistrationchange-getevent.md) | Gets the next pending registration event. |
| [ISyncRegistrationChange::GetInstanceId](..\syncregistration\nf-syncregistration-isyncregistrationchange-getinstanceid.md) | Gets the instance ID of the synchronization provider or synchronization provider configuration UI associated with the event. |
| [ISyncSessionExtendedErrorInfo::GetSyncProviderWithError](..\winsync\nf-winsync-isyncsessionextendederrorinfo-getsyncproviderwitherror.md) | Gets the ISyncProvider interface of the provider that caused synchronization to fail. |
| [ISyncSessionState2::GetSessionErrorStatus](..\winsync\nf-winsync-isyncsessionstate2-getsessionerrorstatus.md) | Gets the error value that indicates why the synchronization session failed. |
| [ISyncSessionState2::SetProviderWithError](..\winsync\nf-winsync-isyncsessionstate2-setproviderwitherror.md) | Indicates which provider caused synchronization to fail. |
| [ISyncSessionState::GetForgottenKnowledgeRecoveryRangeEnd](..\winsync\nf-winsync-isyncsessionstate-getforgottenknowledgerecoveryrangeend.md) | Gets the upper bound of the recovery range when the session is performing forgotten knowledge recovery. |
| [ISyncSessionState::GetForgottenKnowledgeRecoveryRangeStart](..\winsync\nf-winsync-isyncsessionstate-getforgottenknowledgerecoveryrangestart.md) | Gets the lower bound of the recovery range when the session is performing forgotten knowledge recovery. |
| [ISyncSessionState::GetInfoForChangeApplication](..\winsync\nf-winsync-isyncsessionstate-getinfoforchangeapplication.md) | Retrieves stored data for a serialized change applier. |
| [ISyncSessionState::IsCanceled](..\winsync\nf-winsync-isyncsessionstate-iscanceled.md) | Indicates whether the synchronization session has been canceled. |
| [ISyncSessionState::LoadInfoFromChangeApplication](..\winsync\nf-winsync-isyncsessionstate-loadinfofromchangeapplication.md) | Stores data for a serialized change applier. |
| [ISyncSessionState::OnProgress](..\winsync\nf-winsync-isyncsessionstate-onprogress.md) | Reports synchronization progress to the application. |
| [ISyncSessionState::SetForgottenKnowledgeRecoveryRange](..\winsync\nf-winsync-isyncsessionstate-setforgottenknowledgerecoveryrange.md) | Sets the recovery range when the session is performing forgotten knowledge recovery. |
| [ISynchronousDataRetriever::GetIdParameters](..\winsync\nf-winsync-isynchronousdataretriever-getidparameters.md) | Gets the ID format schema of the provider. |
| [ISynchronousDataRetriever::LoadChangeData](..\winsync\nf-winsync-isynchronousdataretriever-loadchangedata.md) | Retrieves item data for a change. |
