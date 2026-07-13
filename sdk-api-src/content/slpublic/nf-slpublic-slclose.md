---
UID: NF:slpublic.SLClose
title: SLClose function (slpublic.h)
description: Closes the Software Licensing Client (SLC) context handle.
helpviewer_keywords: ["SLClose","SLClose function [Security]","security.slclose","slpublic/SLClose"]
old-location: security\slclose.htm
tech.root: security
ms.assetid: a2483fa2-cdd6-48b8-861f-34fd5efc34df
ms.date: 12/05/2018
ms.keywords: SLClose, SLClose function [Security], security.slclose, slpublic/SLClose
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
 - SLClose
 - slpublic/SLClose
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
 - SLClose
---

# SLClose function


## -description

Closes the Software Licensing Client (SLC) context handle. When this function is called,
	the associated context on the Software Licensing Service (SLS) is released.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.

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
</table>

