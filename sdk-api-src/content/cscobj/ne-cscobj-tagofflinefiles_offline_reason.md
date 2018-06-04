---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tagOFFLINEFILES_OFFLINE_REASON enumeration


## -description


Indicates the reason why an item is offline.


## -enum-fields




### -field OFFLINEFILES_OFFLINE_REASON_UNKNOWN

The reason is unknown because the method failed.


### -field OFFLINEFILES_OFFLINE_REASON_NOT_APPLICABLE

The item is online.


### -field OFFLINEFILES_OFFLINE_REASON_CONNECTION_FORCED


<a href="https://msdn.microsoft.com/83b082b4-5845-44b7-9456-f00b357e345a">IOfflineFilesConnectionInfo::GetConnectState</a> returns this value if the item is offline because the item's scope was forced offline using the <a href="https://msdn.microsoft.com/cb32238d-c8f2-4228-8472-4a699b24c621">IOfflineFilesConnectionInfo::TransitionOffline</a> method.  When an item has been transitioned offline by the Work Offline button in Windows Explorer, the offline reason is forced.  When an item is forced offline, its entire scope is also forced offline.  Assuming the remote share is reachable, a scope that is forced offline may be transitioned online using the <a href="https://msdn.microsoft.com/b8cac664-598d-43fd-a77e-e8406c197afc">IOfflineFilesConnectionInfo::TransitionOnline</a> method.


### -field OFFLINEFILES_OFFLINE_REASON_CONNECTION_SLOW


<a href="https://msdn.microsoft.com/83b082b4-5845-44b7-9456-f00b357e345a">IOfflineFilesConnectionInfo::GetConnectState</a> returns this value if the item is offline because the item's connection is considered slow.  The parameters that define a slow connection are defined by Group Policy.  When an item is offline because of a slow connection, its entire scope is also offline for the same reason.  Assuming the remote share is reachable, a scope that is offline because of a slow connection may be transitioned online using the <a href="https://msdn.microsoft.com/b8cac664-598d-43fd-a77e-e8406c197afc">IOfflineFilesConnectionInfo::TransitionOnline</a> method.


### -field OFFLINEFILES_OFFLINE_REASON_CONNECTION_ERROR


<a href="https://msdn.microsoft.com/83b082b4-5845-44b7-9456-f00b357e345a">IOfflineFilesConnectionInfo::GetConnectState</a> returns this value if the item is offline because of an error in network communications.  This normally means that the client computer is disconnected from the network, the server computer is unavailable, or the network shared folder is no longer available.  After the source of the error is corrected and the remote share is again reachable, the scope is automatically transitioned online by Offline Files.


### -field OFFLINEFILES_OFFLINE_REASON_ITEM_VERSION_CONFLICT


<a href="https://msdn.microsoft.com/83b082b4-5845-44b7-9456-f00b357e345a">IOfflineFilesConnectionInfo::GetConnectState</a> returns this value if the item is offline because of an unresolved sync conflict.  While working offline, an item was changed both on the client and the server.  A subsequent sync operation detected the sync conflict and placed a record of that conflict in the sync conflict store.  Sync conflicts may be reviewed in Sync Center's Sync Conflicts folder.  To resolve a conflict programmatically, call <a href="https://msdn.microsoft.com/4a9dd105-ea68-40ce-b1cb-6126ca932095">IOfflineFilesCache::Synchronize</a> with the appropriate conflict resolution mechanism.  For more information, see <b>IOfflineFilesCache::Synchronize</b>.


### -field OFFLINEFILES_OFFLINE_REASON_ITEM_SUSPENDED


<a href="https://msdn.microsoft.com/83b082b4-5845-44b7-9456-f00b357e345a">IOfflineFilesConnectionInfo::GetConnectState</a> returns this value if the item is offline because it was suspended.  Suspending an item is a way to force it to be always available offline.  It is primarily used by Windows features that want to use the offline availability and synchronization capabilities of Offline Files but that also want to control the synchronization.  Suspended items are never synchronized automatically by Offline Files.


## -see-also




<a href="https://msdn.microsoft.com/83b082b4-5845-44b7-9456-f00b357e345a">IOfflineFilesConnectionInfo::GetConnectState</a>



<a href="https://msdn.microsoft.com/42412f42-7a70-4110-88ec-a38b3df7d2da">IOfflineFilesConnectionInfo::SetConnectState</a>
 

 

