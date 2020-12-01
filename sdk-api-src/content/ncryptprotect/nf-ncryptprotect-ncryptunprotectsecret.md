---
UID: NF:ncryptprotect.NCryptUnprotectSecret
title: NCryptUnprotectSecret function (ncryptprotect.h)
description: Decrypts data to a specified protection descriptor.
helpviewer_keywords: ["NCRYPT_SILENT_FLAG","NCRYPT_UNPROTECT_NO_DECRYPT","NCryptUnprotectSecret","NCryptUnprotectSecret function [Security]","ncryptprotect/NCryptUnprotectSecret","security.ncryptunprotectsecret"]
old-location: security\ncryptunprotectsecret.htm
tech.root: security
ms.assetid: F532F0ED-36F4-47E3-B478-089CC083E5D1
ms.date: 12/05/2018
ms.keywords: NCRYPT_SILENT_FLAG, NCRYPT_UNPROTECT_NO_DECRYPT, NCryptUnprotectSecret, NCryptUnprotectSecret function [Security], ncryptprotect/NCryptUnprotectSecret, security.ncryptunprotectsecret
req.header: ncryptprotect.h
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
req.lib: NCrypt.lib
req.dll: NCrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptUnprotectSecret
 - ncryptprotect/NCryptUnprotectSecret
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NCrypt.dll
api_name:
 - NCryptUnprotectSecret
---

# NCryptUnprotectSecret function


## -description

The <b>NCryptUnprotectSecret</b> function decrypts data to a specified protection descriptor. Call <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptprotectsecret">NCryptProtectSecret</a> to encrypt the data.

## -parameters

### -param phDescriptor [out, optional]

Pointer to the protection descriptor handle.

### -param dwFlags [in]

The flag can be zero or a bitwise OR of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_SILENT_FLAG"></a><a id="ncrypt_silent_flag"></a><dl>
<dt><b>NCRYPT_SILENT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Requests that the key service provider not display a user interface.

</td>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_UNPROTECT_NO_DECRYPT"></a><a id="ncrypt_unprotect_no_decrypt"></a><dl>
<dt><b>NCRYPT_UNPROTECT_NO_DECRYPT</b></dt>
</dl>
</td>
<td width="60%">
Decodes only the header of the protected data blob. No actual decryption takes place.

</td>
</tr>
</table>

### -param pbProtectedBlob [in]

Pointer to an array of bytes that contains the data to decrypt.

### -param cbProtectedBlob

The number of bytes in the array pointed to by the <i>pbProtectedBlob</i> parameter.

### -param pMemPara [in, optional]

Pointer to an <a href="/windows/desktop/api/ncrypt/ns-ncrypt-ncrypt_alloc_para">NCRYPT_ALLOC_PARA</a> structure that you can use to specify custom memory management functions. If you set this argument to <b>NULL</b>, the <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> function is used internally to allocate memory and your application must call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release memory pointed to by the <i>ppbData</i> parameter.

### -param hWnd [in, optional]

Handle to the parent window of the user interface, if any, to be displayed.

### -param ppbData [out]

Address of a variable that receives a pointer to the decrypted data.

### -param pcbData [out]

Pointer to a <b>ULONG</b> variable that contains the size, in bytes, of the decrypted data pointed to by the <i>ppbData</i> variable.

## -returns

Returns a status code that indicates the success or failure of the function. Possible return codes include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_BAD_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The dwFlags parameter can only contain <b>NCRYPT_SILENT_FLAG</b> or <b>NCRYPT_UNPROTECT_NO_DECRYPT</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pbProtectedBlob</i>, <i>ppbData</i>, and <i>pcbData</i> parameters cannot be <b>NULL</b>.

The <i>cbData</i> parameter cannot be less than one.

</td>
</tr>
</table>

## -remarks

Use the <b>NCryptUnprotectSecret</b> function to decrypt keys, key material, and passwords. Use the <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a>  and the <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamupdate">NCryptStreamUpdate</a> functions to decrypt larger messages.

## -see-also

<a href="/windows/desktop/SecCNG/cng-dpapi-functions">CNG DPAPI Functions</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptprotectsecret">NCryptProtectSecret</a>