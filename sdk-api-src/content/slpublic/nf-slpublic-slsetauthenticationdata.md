---
UID: NF:slpublic.SLSetAuthenticationData
title: SLSetAuthenticationData function (slpublic.h)
description: Sets authentication data.
helpviewer_keywords: ["SLSetAuthenticationData","SLSetAuthenticationData function [Security]","security.slsetauthenticationdata","slpublic/SLSetAuthenticationData"]
old-location: security\slsetauthenticationdata.htm
tech.root: security
ms.assetid: 68906873-6c49-4221-ad87-1e1f1463c0d4
ms.date: 12/05/2018
ms.keywords: SLSetAuthenticationData, SLSetAuthenticationData function [Security], security.slsetauthenticationdata, slpublic/SLSetAuthenticationData
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
 - SLSetAuthenticationData
 - slpublic/SLSetAuthenticationData
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
 - SLSetAuthenticationData
---

# SLSetAuthenticationData function


## -description

Sets authentication data.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.

### -param cbValue [in, optional]

Type: <b>UINT</b>

The size, in bytes, of the authentication data in <i>pbValue</i>.

### -param pbValue [in, optional]

Type: <b>const BYTE</b>

A pointer to the authentication data.

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
<dt><b>ERROR_INVALID_DATA</b></dt>
<dt>0x8007000D</dt>
</dl>
</td>
<td width="60%">
The format of authentication data is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_AUTHN_WRONG_VERSION</b></dt>
<dt>0xC004F077</dt>
</dl>
</td>
<td width="60%">
The security version is wrong.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_NOT_SUPPORTED</b></dt>
<dt>0xC004F016</dt>
</dl>
</td>
<td width="60%">
The authentication data format is not supported.

</td>
</tr>
</table>

