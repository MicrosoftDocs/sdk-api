---
UID: NF:ncryptprotect.NCryptProtectSecret
title: NCryptProtectSecret function (ncryptprotect.h)
description: Encrypts data to a specified protection descriptor.
helpviewer_keywords: ["NCRYPT_SILENT_FLAG","NCryptProtectSecret","NCryptProtectSecret function [Security]","ncryptprotect/NCryptProtectSecret","security.ncryptprotectsecret"]
old-location: security\ncryptprotectsecret.htm
tech.root: security
ms.assetid: 8726F92B-34D5-4696-8803-3D7F50F1006D
ms.date: 12/05/2018
ms.keywords: NCRYPT_SILENT_FLAG, NCryptProtectSecret, NCryptProtectSecret function [Security], ncryptprotect/NCryptProtectSecret, security.ncryptprotectsecret
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
 - NCryptProtectSecret
 - ncryptprotect/NCryptProtectSecret
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
 - NCryptProtectSecret
---

# NCryptProtectSecret function


## -description

The <b>NCryptProtectSecret</b> function encrypts data to a specified protection descriptor. Call <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptunprotectsecret">NCryptUnprotectSecret</a> to decrypt the data.

## -parameters

### -param hDescriptor [in]

Handle of the protection descriptor object. Create the handle by calling <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor">NCryptCreateProtectionDescriptor</a>.

### -param dwFlags [in]

The flag can be zero or the following value.

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
</table>

### -param pbData [in]

Pointer to the byte array to be protected.

### -param cbData [in]

Number of bytes in the binary array specified by the <i>pbData</i> parameter.

### -param pMemPara [in, optional]

Pointer to an <a href="/windows/desktop/api/ncrypt/ns-ncrypt-ncrypt_alloc_para">NCRYPT_ALLOC_PARA</a> structure that you can use to specify custom memory management functions. If you set this argument to <b>NULL</b>, the <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> function is used internally to allocate memory and your application must call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release memory pointed to by the <i>ppbProtectedBlob</i> parameter.

### -param hWnd [in, optional]

Handle to the parent window of the user interface, if any, to be displayed.

### -param ppbProtectedBlob [out]

Address of a variable that receives a pointer to the encrypted data.

### -param pcbProtectedBlob [out]

Pointer to a <b>ULONG</b> variable that contains the size, in bytes, of the encrypted data pointed to by the <i>ppbProtectedBlob</i> variable.

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
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pbData</i>, <i>ppbProtectedBlob</i>, and <i>pcbProtectedBlob</i> parameters cannot be <b>NULL</b>.

The <i>cbData</i> parameter cannot be less than one.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to allocate the content encryption key.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified by the <i>hDescriptor</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

Use the <b>NCryptProtectSecret</b> function to protect keys, key material, and passwords. Use the <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a> and the <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamupdate">NCryptStreamUpdate</a> functions to encrypt larger messages.

## -see-also

<a href="/windows/desktop/SecCNG/cng-dpapi-functions">CNG DPAPI Functions</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor">NCryptCreateProtectionDescriptor</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptunprotectsecret">NCryptUnprotectSecret</a>