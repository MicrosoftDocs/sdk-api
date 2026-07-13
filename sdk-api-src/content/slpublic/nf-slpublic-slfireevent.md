---
UID: NF:slpublic.SLFireEvent
title: SLFireEvent function (slpublic.h)
description: Sends a specified event to a registered listener.
helpviewer_keywords: ["SLFireEvent","SLFireEvent function [Security]","security.slfireevent","slpublic/SLFireEvent"]
old-location: security\slfireevent.htm
tech.root: security
ms.assetid: 7d66526a-f83a-4a7d-9691-e8ee9ec9a135
ms.date: 12/05/2018
ms.keywords: SLFireEvent, SLFireEvent function [Security], security.slfireevent, slpublic/SLFireEvent
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
 - SLFireEvent
 - slpublic/SLFireEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-security-slc-l1-1-0.dll
 - Slc.dll
api_name:
 - SLFireEvent
---

# SLFireEvent function


## -description

Sends a specified event to a registered listener.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.

### -param pwszEventId [in]

Type: <b>PCWSTR</b>

The ID of the event to be fired.

### -param pApplicationId [in]

Type: <b>const SLID*</b>

A pointer to the application ID.

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
<dt><b>E_ACCESSDENIED</b></dt>
<dt>0x80070005</dt>
</dl>
</td>
<td width="60%">
Access denied (API requires admin privileges).

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

