---
UID: NF:ncryptprotect.NCryptStreamOpenToUnprotect
title: NCryptStreamOpenToUnprotect function (ncryptprotect.h)
description: Opens a stream object that can be used to decrypt large amounts of data to the same protection descriptor used for encryption. (NCryptStreamOpenToUnprotect)
helpviewer_keywords: ["NCRYPT_SILENT_FLAG","NCryptStreamOpenToUnprotect","NCryptStreamOpenToUnprotect function [Security]","ncryptprotect/NCryptStreamOpenToUnprotect","security.ncryptstreamopentounprotect"]
old-location: security\ncryptstreamopentounprotect.htm
tech.root: security
ms.assetid: 9848082E-EDDA-4DA1-9896-42EAF2ADFAB4
ms.date: 12/05/2018
ms.keywords: NCRYPT_SILENT_FLAG, NCryptStreamOpenToUnprotect, NCryptStreamOpenToUnprotect function [Security], ncryptprotect/NCryptStreamOpenToUnprotect, security.ncryptstreamopentounprotect
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
 - NCryptStreamOpenToUnprotect
 - ncryptprotect/NCryptStreamOpenToUnprotect
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
 - NCryptStreamOpenToUnprotect
---

# NCryptStreamOpenToUnprotect function


## -description

The <b>NCryptStreamOpenToUnprotect</b> function opens a stream object that can be used to decrypt large amounts of data to the same  protection descriptor used for encryption. Call <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamupdate">NCryptStreamUpdate</a> to perform the decryption. To decrypt smaller messages such as keys and passwords, call <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptunprotectsecret">NCryptUnprotectSecret</a>.

## -parameters

### -param pStreamInfo [in]

Pointer to an <a href="/windows/desktop/api/ncryptprotect/ns-ncryptprotect-ncrypt_protect_stream_info">NCRYPT_PROTECT_STREAM_INFO</a> structure that contains the address of a user defined callback function to receive the decrypted data and a pointer to user-defined context data.

### -param dwFlags

A flag that specifies additional information for the key service provider. This can be zero or the following value.

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

### -param phStream [out]

Pointer to the handle of the decrypted stream of data.

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
The dwFlags parameter must contain zero (0) or <b>NCRYPT_SILENT_FLAG</b>.

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

The <b>NCryptStreamOpenToUnprotect</b> function  creates an internal stream object that can be used to encrypt large messages. You cannot use the object directly. Instead, you must use the object handle returned by this function.

Call this function before calling the <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamupdate">NCryptStreamUpdate</a> function. If you are encrypting a large file, use <b>NCryptStreamUpdate</b> in a loop that advances through the file block by block, encrypting each block as it advances and notifying your callback when each block is finished. For more information, see <b>NCryptStreamUpdate</b>.

The <b>NCryptStreamOpenToUnprotect</b> function retrieves the unencrypted protection descriptor rule string from the stream header. The rule string is placed in the header by the <b>NCryptStreamOpenToUnprotect</b> function.

## -see-also

<a href="/windows/desktop/SecCNG/cng-dpapi-functions">CNG DPAPI Functions</a>



<a href="/windows/desktop/api/ncryptprotect/ns-ncryptprotect-ncrypt_protect_stream_info">NCRYPT_PROTECT_STREAM_INFO</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamclose">NCryptStreamClose</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect">NCryptStreamOpenToProtect</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptstreamupdate">NCryptStreamUpdate</a>
