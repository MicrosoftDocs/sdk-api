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

# ISyncMgrSynchronizeInvoke::UpdateItems


## -description


Programmatically starts an update for specified items.


## -parameters




### -param dwInvokeFlags [in]

Type: <b>DWORD</b>

Specifies how an item should be invoked using the <a href="https://msdn.microsoft.com/6526e048-b7a8-4822-afd7-30f04a3039eb">SYNCMGRINVOKEFLAGS</a> enumeration values.


### -param clsid




### -param cbCookie [in]

Type: <b>DWORD</b>

The size of <i>pCookie</i> data, in bytes.


### -param pCookie [in]

Type: <b>const BYTE*</b>

A pointer to a private token that identifies an application. The token is passed in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method.


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



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>



<a href="https://msdn.microsoft.com/6526e048-b7a8-4822-afd7-30f04a3039eb">SYNCMGRINVOKEFLAGS</a>
 

 

