---
UID: NF:ncryptprotect.NCryptStreamOpenToProtect
title: NCryptStreamOpenToProtect function (ncryptprotect.h)
description: Opens a stream object that can be used to encrypt large amounts of data to a given protection descriptor.
helpviewer_keywords: ["NCRYPT_SILENT_FLAG","NCryptStreamOpenToProtect","NCryptStreamOpenToProtect function [Security]","ncryptprotect/NCryptStreamOpenToProtect","security.ncryptstreamopentoprotect"]
old-location: security\ncryptstreamopentoprotect.htm
tech.root: security
ms.assetid: 7DE74BB1-1B84-4721-BE4A-4D2661E93E00
ms.date: 12/05/2018
ms.keywords: NCRYPT_SILENT_FLAG, NCryptStreamOpenToProtect, NCryptStreamOpenToProtect function [Security], ncryptprotect/NCryptStreamOpenToProtect, security.ncryptstreamopentoprotect
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
 - NCryptStreamOpenToProtect
 - ncryptprotect/NCryptStreamOpenToProtect
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
 - NCryptStreamOpenToProtect
---

# NCryptStreamOpenToProtect function


## -description

The <b>NCryptStreamOpenToProtect</b> function opens a stream object that can be used to encrypt large amounts of data  to a given protection descriptor. Call <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamupdate">NCryptStreamUpdate</a> to encrypt the content. To encrypt smaller messages such as keys and passwords, call <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptprotectsecret">NCryptProtectSecret</a>.

## -parameters

### -param hDescriptor [in]

Handle of the protection descriptor. Create the handle by calling <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor">NCryptCreateProtectionDescriptor</a>.

### -param dwFlags

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

### -param hWnd [in, optional]

Handle to the parent window of the user interface, if any, to be displayed.

### -param pStreamInfo [in]

Pointer to an <a href="/windows/desktop/api/ncryptprotect/ns-ncryptprotect-ncrypt_protect_stream_info">NCRYPT_PROTECT_STREAM_INFO</a> structure that contains the address of a user defined callback function to receive the encrypted data and a pointer to user-defined context data.

### -param phStream [out]

Pointer to the stream object handle.

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
The dwFlags parameter must contain zero (0), <b>NCRYPT_MACHINE_KEY_FLAG</b>, or <b>NCRYPT_SILENT_FLAG</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>phStream</i> and <i>pStreamInfo</i> parameters cannot be <b>NULL</b>.

The callback function pointed to by the <b>pfnStreamOutput</b> member of the <a href="/windows/desktop/api/ncryptprotect/ns-ncryptprotect-ncrypt_protect_stream_info">NCRYPT_PROTECT_STREAM_INFO</a> structure pointed to by the <i>pStreamInfo</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to allocate a data stream.

</td>
</tr>
</table>

## -remarks

The <b>NCryptStreamOpenToProtect</b> function creates an internal stream object that can be used to encrypt large messages. You cannot use the object directly. Instead, you must use the object handle returned by this function.

Call this function before calling the <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamupdate">NCryptStreamUpdate</a> function. If you are encrypting a large file, use <b>NCryptStreamUpdate</b> in a loop that advances through the file block by block, encrypting each block as it advances and notifying your callback when each block is finished. For more information, see <b>NCryptStreamUpdate</b>.

The <b>NCryptStreamOpenToProtect</b> function writes the unencrypted protection descriptor rule string to the stream object header so that <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a> will be able to start the decrypting the stream by using the same protector used during encryption.

## -see-also

<a href="/windows/desktop/SecCNG/cng-dpapi-functions">CNG DPAPI Functions</a>



<a href="/windows/desktop/api/ncryptprotect/ns-ncryptprotect-ncrypt_protect_stream_info">NCRYPT_PROTECT_STREAM_INFO</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor">NCryptCreateProtectionDescriptor</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamclose">NCryptStreamClose</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect">NCryptStreamOpenToUnprotect</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamupdate">NCryptStreamUpdate</a>