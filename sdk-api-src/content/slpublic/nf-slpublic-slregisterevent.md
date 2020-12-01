---
UID: NF:slpublic.SLRegisterEvent
title: SLRegisterEvent function (slpublic.h)
description: Registers an event in the SL service.
helpviewer_keywords: ["SLRegisterEvent","SLRegisterEvent function [Security]","security.slregisterevent","slpublic/SLRegisterEvent"]
old-location: security\slregisterevent.htm
tech.root: security
ms.assetid: a18f58d4-c8e7-4974-a015-e4941e834e79
ms.date: 12/05/2018
ms.keywords: SLRegisterEvent, SLRegisterEvent function [Security], security.slregisterevent, slpublic/SLRegisterEvent
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
 - SLRegisterEvent
 - slpublic/SLRegisterEvent
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
 - SLRegisterEvent
---

# SLRegisterEvent function


## -description

 Registers an event in the SL service. The caller can receive notifications when the registered event is fired.

## -parameters

### -param hSLC [in, optional]

Type: <b>HSLC</b>

The handle to the current SLC session.

### -param pwszEventId [in]

Type: <b>PCWSTR</b>

The predefined SL event identifier.

### -param pApplicationId [in]

Type: <b>const SLID*</b>

A pointer to the  application ID to which the event will be registered.

### -param hEvent [in]

Type: <b>HANDLE</b>

 The event handle used for notification.

## -returns

Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
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
</table>

