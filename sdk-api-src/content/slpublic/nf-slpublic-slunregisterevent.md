---
UID: NF:slpublic.SLUnregisterEvent
title: SLUnregisterEvent function (slpublic.h)
description: Unregisters a registered event in the SL service.
helpviewer_keywords: ["SLUnregisterEvent","SLUnregisterEvent function [Security]","security.slunregisterevent","slpublic/SLUnregisterEvent"]
old-location: security\slunregisterevent.htm
tech.root: security
ms.assetid: 0fd02eb4-16d9-4892-b50c-3f9b0ead8478
ms.date: 12/05/2018
ms.keywords: SLUnregisterEvent, SLUnregisterEvent function [Security], security.slunregisterevent, slpublic/SLUnregisterEvent
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Slc.lib
req.dll: Slc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SLUnregisterEvent
 - slpublic/SLUnregisterEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Slc.dll
api_name:
 - SLUnregisterEvent
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

