---
UID: NF:slpublic.SLGetAuthenticationResult
title: SLGetAuthenticationResult function (slpublic.h)
description: Gets the authentication results.
helpviewer_keywords: ["SLGetAuthenticationResult","SLGetAuthenticationResult function [Security]","security.slgetauthenticationresult","slpublic/SLGetAuthenticationResult"]
old-location: security\slgetauthenticationresult.htm
tech.root: security
ms.assetid: 8f30ac28-92a0-41f5-b076-eda7014fb526
ms.date: 12/05/2018
ms.keywords: SLGetAuthenticationResult, SLGetAuthenticationResult function [Security], security.slgetauthenticationresult, slpublic/SLGetAuthenticationResult
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
 - SLGetAuthenticationResult
 - slpublic/SLGetAuthenticationResult
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
 - SLGetAuthenticationResult
---

# SLGetAuthenticationResult function


## -description

Gets the authentication results.

## -parameters

### -param hSLC [in]

Type: <b>HSLC</b>

The handle to the current SLC context.

### -param pcbValue [out]

Type: <b>UINT*</b>

A pointer to the size, in bytes, of the authentication result.

### -param ppbValue [out]

Type: <b>PBYTE*</b>

A pointer to the authentication result. When finished using the memory, free it by calling the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

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
<dt><b>SL_E_AUTHN_MISMATCHED_KEY</b></dt>
<dt>0xC004F078</dt>
</dl>
</td>
<td width="60%">
The key used in the <a href="/windows/desktop/api/slpublic/nf-slpublic-slsetauthenticationdata">SLSetAuthenticationData</a> function call is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_AUTHN_CANT_VERIFY</b></dt>
<dt>0xC004F07A</dt>
</dl>
</td>
<td width="60%">
The authentication cannot be completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_AUTHN_CHALLENGE_NOT_SET</b></dt>
<dt>0xC004F079</dt>
</dl>
</td>
<td width="60%">
The authentication data (challenge) is not set.

</td>
</tr>
</table>