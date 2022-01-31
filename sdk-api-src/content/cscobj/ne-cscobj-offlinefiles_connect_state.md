---
UID: NE:cscobj.tagOFFLINEFILES_CONNECT_STATE
title: OFFLINEFILES_CONNECT_STATE (cscobj.h)
description: Describes the connection state of an item in the Offline Files cache.
helpviewer_keywords: ["OFFLINEFILES_CONNECT_STATE","OFFLINEFILES_CONNECT_STATE enumeration [Offline Files]","OFFLINEFILES_CONNECT_STATE_OFFLINE","OFFLINEFILES_CONNECT_STATE_ONLINE","OFFLINEFILES_CONNECT_STATE_PARTLY_TRANSPARENTLY_CACHED","OFFLINEFILES_CONNECT_STATE_TRANSPARENTLY_CACHED","OFFLINEFILES_CONNECT_STATE_UNKNOWN","cscobj/OFFLINEFILES_CONNECT_STATE","cscobj/OFFLINEFILES_CONNECT_STATE_OFFLINE","cscobj/OFFLINEFILES_CONNECT_STATE_ONLINE","cscobj/OFFLINEFILES_CONNECT_STATE_PARTLY_TRANSPARENTLY_CACHED","cscobj/OFFLINEFILES_CONNECT_STATE_TRANSPARENTLY_CACHED","cscobj/OFFLINEFILES_CONNECT_STATE_UNKNOWN","of.offlinefiles_connect_state"]
old-location: of\offlinefiles_connect_state.htm
tech.root: of
ms.assetid: 48c19b16-6ccb-4580-916d-0d23b69aafcf
ms.date: 12/05/2018
ms.keywords: OFFLINEFILES_CONNECT_STATE, OFFLINEFILES_CONNECT_STATE enumeration [Offline Files], OFFLINEFILES_CONNECT_STATE_OFFLINE, OFFLINEFILES_CONNECT_STATE_ONLINE, OFFLINEFILES_CONNECT_STATE_PARTLY_TRANSPARENTLY_CACHED, OFFLINEFILES_CONNECT_STATE_TRANSPARENTLY_CACHED, OFFLINEFILES_CONNECT_STATE_UNKNOWN, cscobj/OFFLINEFILES_CONNECT_STATE, cscobj/OFFLINEFILES_CONNECT_STATE_OFFLINE, cscobj/OFFLINEFILES_CONNECT_STATE_ONLINE, cscobj/OFFLINEFILES_CONNECT_STATE_PARTLY_TRANSPARENTLY_CACHED, cscobj/OFFLINEFILES_CONNECT_STATE_TRANSPARENTLY_CACHED, cscobj/OFFLINEFILES_CONNECT_STATE_UNKNOWN, of.offlinefiles_connect_state
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
req.typenames: OFFLINEFILES_CONNECT_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagOFFLINEFILES_CONNECT_STATE
 - cscobj/tagOFFLINEFILES_CONNECT_STATE
 - OFFLINEFILES_CONNECT_STATE
 - cscobj/OFFLINEFILES_CONNECT_STATE
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
 - OFFLINEFILES_CONNECT_STATE
---

# OFFLINEFILES_CONNECT_STATE enumeration


## -description

Describes the connection state of an item in the Offline Files cache.

## -enum-fields

### -field OFFLINEFILES_CONNECT_STATE_UNKNOWN:0

Returned by <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">IOfflineFilesConnectionInfo::GetConnectState</a> if the method fails.

### -field OFFLINEFILES_CONNECT_STATE_OFFLINE

Returned by <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">IOfflineFilesConnectionInfo::GetConnectState</a> if the item is offline. Pass this value to <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-setconnectstate">IOfflineFilesConnectionInfo::SetConnectState</a> to transition the item to offline.

### -field OFFLINEFILES_CONNECT_STATE_ONLINE

Returned by <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">IOfflineFilesConnectionInfo::GetConnectState</a> if the item is online. Pass this value to <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-setconnectstate">IOfflineFilesConnectionInfo::SetConnectState</a> to transition the item to online.

### -field OFFLINEFILES_CONNECT_STATE_TRANSPARENTLY_CACHED

Returned by <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">IOfflineFilesConnectionInfo::GetConnectState</a> if the item is transparently cached.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported before Windows Server 2008 R2 and Windows 7.

### -field OFFLINEFILES_CONNECT_STATE_PARTLY_TRANSPARENTLY_CACHED

Returned by <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">IOfflineFilesConnectionInfo::GetConnectState</a> if the item contains both transparently cached data and data that can be made available offline.

<b>Windows Server 2008 and Windows Vista:  </b>This value is not supported before Windows Server 2008 R2 and Windows 7.

## -remarks

Transparently cached data is accessible only when the client is connected to the server.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-getconnectstate">IOfflineFilesConnectionInfo::GetConnectState</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesconnectioninfo-setconnectstate">IOfflineFilesConnectionInfo::SetConnectState</a>
