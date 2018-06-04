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

# SLUnregisterEvent function


## -description


Unregisters a registered event in the SL service.


## -parameters




### -param hSLC [in, optional]

Type: <b>HSLC</b>

The handle to the current SLC session.


### -param pwszEventId [in]

Type: <b>PCWSTR</b>

The predefined SL event identifier that will be unregistered.


### -param pApplicationId [in]

Type: <b>const SLID*</b>

A pointer to the application ID that the event will be unregistered from.


### -param hEvent [in]

Type: <b>HANDLE</b>

The registered event handle.


## -returns



Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise,  it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_INVALID_EVENT_ID</b></dt>
<dt>0xC004F019</dt>
</dl>
</td>
<td width="60%">
The requested event ID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_EVENT_NOT_REGISTERED</b></dt>
<dt>0xC004F01A</dt>
</dl>
</td>
<td width="60%">
The requested event is not registered with the service.

</td>
</tr>
</table>
 



