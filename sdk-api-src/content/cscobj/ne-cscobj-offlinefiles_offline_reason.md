---
UID: NE:cscobj.tagOFFLINEFILES_OFFLINE_REASON
title: OFFLINEFILES_OFFLINE_REASON (cscobj.h)
description: Indicates the reason why an item is offline.
helpviewer_keywords: ["OFFLINEFILES_OFFLINE_REASON","OFFLINEFILES_OFFLINE_REASON enumeration [Offline Files]","OFFLINEFILES_OFFLINE_REASON_CONNECTION_ERROR","OFFLINEFILES_OFFLINE_REASON_CONNECTION_FORCED","OFFLINEFILES_OFFLINE_REASON_CONNECTION_SLOW","OFFLINEFILES_OFFLINE_REASON_ITEM_SUSPENDED","OFFLINEFILES_OFFLINE_REASON_ITEM_VERSION_CONFLICT","OFFLINEFILES_OFFLINE_REASON_NOT_APPLICABLE","OFFLINEFILES_OFFLINE_REASON_UNKNOWN","cscobj/OFFLINEFILES_OFFLINE_REASON","cscobj/OFFLINEFILES_OFFLINE_REASON_CONNECTION_ERROR","cscobj/OFFLINEFILES_OFFLINE_REASON_CONNECTION_FORCED","cscobj/OFFLINEFILES_OFFLINE_REASON_CONNECTION_SLOW","cscobj/OFFLINEFILES_OFFLINE_REASON_ITEM_SUSPENDED","cscobj/OFFLINEFILES_OFFLINE_REASON_ITEM_VERSION_CONFLICT","cscobj/OFFLINEFILES_OFFLINE_REASON_NOT_APPLICABLE","cscobj/OFFLINEFILES_OFFLINE_REASON_UNKNOWN","of.offlinefiles_offline_reason"]
old-location: of\offlinefiles_offline_reason.htm
tech.root: of
ms.assetid: 0c55b7c6-f39d-4e04-bf16-a102c4b7d4fa
ms.date: 12/05/2018
ms.keywords: OFFLINEFILES_OFFLINE_REASON, OFFLINEFILES_OFFLINE_REASON enumeration [Offline Files], OFFLINEFILES_OFFLINE_REASON_CONNECTION_ERROR, OFFLINEFILES_OFFLINE_REASON_CONNECTION_FORCED, OFFLINEFILES_OFFLINE_REASON_CONNECTION_SLOW, OFFLINEFILES_OFFLINE_REASON_ITEM_SUSPENDED, OFFLINEFILES_OFFLINE_REASON_ITEM_VERSION_CONFLICT, OFFLINEFILES_OFFLINE_REASON_NOT_APPLICABLE, OFFLINEFILES_OFFLINE_REASON_UNKNOWN, cscobj/OFFLINEFILES_OFFLINE_REASON, cscobj/OFFLINEFILES_OFFLINE_REASON_CONNECTION_ERROR, cscobj/OFFLINEFILES_OFFLINE_REASON_CONNECTION_FORCED, cscobj/OFFLINEFILES_OFFLINE_REASON_CONNECTION_SLOW, cscobj/OFFLINEFILES_OFFLINE_REASON_ITEM_SUSPENDED, cscobj/OFFLINEFILES_OFFLINE_REASON_ITEM_VERSION_CONFLICT, cscobj/OFFLINEFILES_OFFLINE_REASON_NOT_APPLICABLE, cscobj/OFFLINEFILES_OFFLINE_REASON_UNKNOWN, of.offlinefiles_offline_reason
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OFFLINEFILES_OFFLINE_REASON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOFFLINEFILES_OFFLINE_REASON
 - cscobj/tagOFFLINEFILES_OFFLINE_REASON
 - OFFLINEFILES_OFFLINE_REASON
 - cscobj/OFFLINEFILES_OFFLINE_REASON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CscObj.h
api_name:
 - OFFLINEFILES_OFFLINE_REASON
---

# OFFLINEFILES_OFFLINE_REASON enumeration


## -description

Indicates the reason why an item is offline.

## -enum-fields

### -field OFFLINEFILES_OFFLINE_REASON_UNKNOWN:0

The reason is unknown because the method failed.

### -field OFFLINEFILES_OFFLINE_REASON_NOT_APPLICABLE

The item is online.

### -field OFFLINEFILES_OFFLINE_REASON_CONNECTION_FORCED

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">IOfflineFilesConnectionInfo::GetConnectState</a> returns this value if the item is offline because the item's scope was forced offline using the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-transitionoffline">IOfflineFilesConnectionInfo::TransitionOffline</a> method.  When an item has been transitioned offline by the Work Offline button in Windows Explorer, the offline reason is forced.  When an item is forced offline, its entire scope is also forced offline.  Assuming the remote share is reachable, a scope that is forced offline may be transitioned online using the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-transitiononline">IOfflineFilesConnectionInfo::TransitionOnline</a> method.

### -field OFFLINEFILES_OFFLINE_REASON_CONNECTION_SLOW

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">IOfflineFilesConnectionInfo::GetConnectState</a> returns this value if the item is offline because the item's connection is considered slow.  The parameters that define a slow connection are defined by Group Policy.  When an item is offline because of a slow connection, its entire scope is also offline for the same reason.  Assuming the remote share is reachable, a scope that is offline because of a slow connection may be transitioned online using the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-transitiononline">IOfflineFilesConnectionInfo::TransitionOnline</a> method.

### -field OFFLINEFILES_OFFLINE_REASON_CONNECTION_ERROR

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">IOfflineFilesConnectionInfo::GetConnectState</a> returns this value if the item is offline because of an error in network communications.  This normally means that the client computer is disconnected from the network, the server computer is unavailable, or the network shared folder is no longer available.  After the source of the error is corrected and the remote share is again reachable, the scope is automatically transitioned online by Offline Files.

### -field OFFLINEFILES_OFFLINE_REASON_ITEM_VERSION_CONFLICT

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">IOfflineFilesConnectionInfo::GetConnectState</a> returns this value if the item is offline because of an unresolved sync conflict.  While working offline, an item was changed both on the client and the server.  A subsequent sync operation detected the sync conflict and placed a record of that conflict in the sync conflict store.  Sync conflicts may be reviewed in Sync Center's Sync Conflicts folder.  To resolve a conflict programmatically, call <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-synchronize">IOfflineFilesCache::Synchronize</a> with the appropriate conflict resolution mechanism.  For more information, see <b>IOfflineFilesCache::Synchronize</b>.

### -field OFFLINEFILES_OFFLINE_REASON_ITEM_SUSPENDED

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">IOfflineFilesConnectionInfo::GetConnectState</a> returns this value if the item is offline because it was suspended.  Suspending an item is a way to force it to be always available offline.  It is primarily used by Windows features that want to use the offline availability and synchronization capabilities of Offline Files but that also want to control the synchronization.  Suspended items are never synchronized automatically by Offline Files.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">IOfflineFilesConnectionInfo::GetConnectState</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-setconnectstate">IOfflineFilesConnectionInfo::SetConnectState</a>
