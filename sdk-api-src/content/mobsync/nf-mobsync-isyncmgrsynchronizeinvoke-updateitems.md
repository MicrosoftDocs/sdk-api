---
UID: NF:mobsync.ISyncMgrSynchronizeInvoke.UpdateItems
title: ISyncMgrSynchronizeInvoke::UpdateItems
author: windows-sdk-content
description: Programmatically starts an update for specified items.
old-location: shell\syncmgr_isyncmgrsynchronizeinvoke_updateitems.htm
tech.root: shell
ms.assetid: 7a646d11-a84c-44c1-b52b-ffd364cc2ac3
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ISyncMgrSynchronizeInvoke interface [Windows Shell],UpdateItems method, ISyncMgrSynchronizeInvoke.UpdateItems, ISyncMgrSynchronizeInvoke::UpdateItems, UpdateItems, UpdateItems method [Windows Shell], UpdateItems method [Windows Shell],ISyncMgrSynchronizeInvoke interface, mobsync/ISyncMgrSynchronizeInvoke::UpdateItems, shell.syncmgr_isyncmgrsynchronizeinvoke_updateitems, syncmgr.isyncmgrsynchronizeinvoke_updateitems
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Mobsync.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronizeInvoke.UpdateItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSynchronizeInvoke::UpdateItems


## -description


Programmatically starts an update for specified items.


## -parameters




### -param dwInvokeFlags [in]

Type: <b>DWORD</b>

Specifies how an item should be invoked using the <a href="https://msdn.microsoft.com/6526e048-b7a8-4822-afd7-30f04a3039eb">SYNCMGRINVOKEFLAGS</a> enumeration values.


### -param clsid

TBD


### -param cbCookie [in]

Type: <b>DWORD</b>

The size of <i>pCookie</i> data, in bytes.


### -param pCookie [in]

Type: <b>const BYTE*</b>

A pointer to a private token that identifies an application. The token is passed in the <a href="https://msdn.microsoft.com/4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10">Initialize</a> method.


#### - CLSID [in]

Type: <b>REFCLSID</b>

The CLSID of a registered application to be invoked for an update.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED and E_OUTOFMEMORY, and the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The synchronization is successfully updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The errors occur during a synchronization update.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/993fd482-39e0-4966-ba71-eed7e4b54f72">ISyncMgrSynchronizeInvoke</a>



<a href="https://msdn.microsoft.com/4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10">Initialize</a>



<a href="https://msdn.microsoft.com/6526e048-b7a8-4822-afd7-30f04a3039eb">SYNCMGRINVOKEFLAGS</a>
 

 

