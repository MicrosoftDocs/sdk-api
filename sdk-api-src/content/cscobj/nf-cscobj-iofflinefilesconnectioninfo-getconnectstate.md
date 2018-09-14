---
UID: NF:cscobj.IOfflineFilesConnectionInfo.GetConnectState
title: IOfflineFilesConnectionInfo::GetConnectState
author: windows-sdk-content
description: Determines whether an item is online or offline and, if offline, why.
old-location: of\iofflinefilesconnectioninfo_getconnectstate.htm
tech.root: OfflineFiles
ms.assetid: 83b082b4-5845-44b7-9456-f00b357e345a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetConnectState, GetConnectState method [Offline Files], GetConnectState method [Offline Files],IOfflineFilesConnectionInfo interface, IOfflineFilesConnectionInfo interface [Offline Files],GetConnectState method, IOfflineFilesConnectionInfo.GetConnectState, IOfflineFilesConnectionInfo::GetConnectState, cscobj/IOfflineFilesConnectionInfo::GetConnectState, of.iofflinefilesconnectioninfo_getconnectstate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesConnectionInfo::GetConnectState


## -description


Determines whether an item is online or offline and, if offline, why.


## -parameters




### -param pConnectState [out]

Receives an <a href="https://msdn.microsoft.com/en-us/library/Bb530644(v=VS.85).aspx">OFFLINEFILES_CONNECT_STATE</a> enumeration value that indicates whether the item is online or offline.

<div class="alert"><b>Note</b>  This value sets the Offline Status property value in Windows Explorer.</div>
<div> </div>

### -param pOfflineReason [out]

If the item is offline, this parameter receives an <a href="https://msdn.microsoft.com/en-us/library/Bb530649(v=VS.85).aspx">OFFLINEFILES_OFFLINE_REASON</a> enumeration value that indicates why the item is offline.

<div class="alert"><b>Note</b>  This value generates the parenthesized suffix in the Offline Status property value in Windows Explorer when the status is offline.</div>
<div> </div>

## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



This method requires that the item have connection state information.  If that information is unavailable at the time of this method call, the method call will initiate the extra query of the cache item to obtain the current connection state.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530511(v=VS.85).aspx">IOfflineFilesConnectionInfo</a>
 

 

