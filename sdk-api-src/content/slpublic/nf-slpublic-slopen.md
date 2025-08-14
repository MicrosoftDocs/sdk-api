---
UID: NF:slpublic.SLOpen
title: SLOpen function (slpublic.h)
description: Initializes the Software Licensing Client (SLC) and connects SLC to the Software Licensing Service (SLS).
helpviewer_keywords: ["SLOpen","SLOpen function [Security]","security.slopen","slpublic/SLOpen"]
old-location: security\slopen.htm
tech.root: security
ms.assetid: 79a09cf3-cf6f-479a-89c7-27f5fcee3186
ms.date: 12/05/2018
ms.keywords: SLOpen, SLOpen function [Security], security.slopen, slpublic/SLOpen
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
 - SLOpen
 - slpublic/SLOpen
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
 - SLOpen
---

# SLOpen function


## -description

Initializes the Software Licensing Client (SLC)
	and connects SLC to the Software Licensing Service (SLS). 
	If the function succeeds, a context handle is returned for subsequent calls.

## -parameters

### -param phSLC [out]

Type: <b>HSLC*</b>

A pointer to a context handle returned from the Software Licensing Service.

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
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
</table>

