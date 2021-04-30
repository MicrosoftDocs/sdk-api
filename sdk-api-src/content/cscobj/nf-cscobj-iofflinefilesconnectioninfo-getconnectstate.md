---
UID: NF:cscobj.IOfflineFilesConnectionInfo.GetConnectState
title: IOfflineFilesConnectionInfo::GetConnectState (cscobj.h)
description: Determines whether an item is online or offline and, if offline, why.
helpviewer_keywords: ["GetConnectState","GetConnectState method [Offline Files]","GetConnectState method [Offline Files]","IOfflineFilesConnectionInfo interface","IOfflineFilesConnectionInfo interface [Offline Files]","GetConnectState method","IOfflineFilesConnectionInfo.GetConnectState","IOfflineFilesConnectionInfo::GetConnectState","cscobj/IOfflineFilesConnectionInfo::GetConnectState","of.iofflinefilesconnectioninfo_getconnectstate"]
old-location: of\iofflinefilesconnectioninfo_getconnectstate.htm
tech.root: of
ms.assetid: 83b082b4-5845-44b7-9456-f00b357e345a
ms.date: 12/05/2018
ms.keywords: GetConnectState, GetConnectState method [Offline Files], GetConnectState method [Offline Files],IOfflineFilesConnectionInfo interface, IOfflineFilesConnectionInfo interface [Offline Files],GetConnectState method, IOfflineFilesConnectionInfo.GetConnectState, IOfflineFilesConnectionInfo::GetConnectState, cscobj/IOfflineFilesConnectionInfo::GetConnectState, of.iofflinefilesconnectioninfo_getconnectstate
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesConnectionInfo::GetConnectState
 - cscobj/IOfflineFilesConnectionInfo::GetConnectState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesConnectionInfo.GetConnectState
---

# IOfflineFilesConnectionInfo::GetConnectState


## -description

Determines whether an item is online or offline and, if offline, why.

## -parameters

### -param pConnectState [out]

Receives an <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_connect_state">OFFLINEFILES_CONNECT_STATE</a> enumeration value that indicates whether the item is online or offline.

<div class="alert"><b>Note</b>  This value sets the Offline Status property value in Windows Explorer.</div>
<div> </div>

### -param pOfflineReason [out]

If the item is offline, this parameter receives an <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_offline_reason">OFFLINEFILES_OFFLINE_REASON</a> enumeration value that indicates why the item is offline.

<div class="alert"><b>Note</b>  This value generates the parenthesized suffix in the Offline Status property value in Windows Explorer when the status is offline.</div>
<div> </div>

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

This method requires that the item have connection state information.  If that information is unavailable at the time of this method call, the method call will initiate the extra query of the cache item to obtain the current connection state.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesconnectioninfo">IOfflineFilesConnectionInfo</a>