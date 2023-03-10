---
UID: NF:imagehlp.ImageGetDigestStream
title: ImageGetDigestStream function (imagehlp.h)
description: Retrieves the requested data from the specified image file.
helpviewer_keywords: ["CERT_PE_IMAGE_DIGEST_ALL_IMPORT_INFO","CERT_PE_IMAGE_DIGEST_DEBUG_INFO","CERT_PE_IMAGE_DIGEST_RESOURCES","ImageGetDigestStream","ImageGetDigestStream function","_win32_imagegetdigeststream","base.imagegetdigeststream","imagehlp/ImageGetDigestStream"]
old-location: base\imagegetdigeststream.htm
tech.root: Debug
ms.assetid: e4560609-5b10-453f-a9a6-c5483d88cd64
ms.date: 12/05/2018
ms.keywords: CERT_PE_IMAGE_DIGEST_ALL_IMPORT_INFO, CERT_PE_IMAGE_DIGEST_DEBUG_INFO, CERT_PE_IMAGE_DIGEST_RESOURCES, ImageGetDigestStream, ImageGetDigestStream function, _win32_imagegetdigeststream, base.imagegetdigeststream, imagehlp/ImageGetDigestStream
req.header: imagehlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Imagehlp.lib
req.dll: Imagehlp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageGetDigestStream
 - imagehlp/ImageGetDigestStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imagehlp.dll
api_name:
 - ImageGetDigestStream
---

# ImageGetDigestStream function


## -description

Retrieves the requested data from the specified image file.

## -parameters

### -param FileHandle [in]

A handle to the image file. This handle must be opened for FILE_READ_DATA access.

### -param DigestLevel [in]

The aspects of the image that are to be included in the returned data stream. This parameter can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_PE_IMAGE_DIGEST_ALL_IMPORT_INFO"></a><a id="cert_pe_image_digest_all_import_info"></a><dl>
<dt><b>CERT_PE_IMAGE_DIGEST_ALL_IMPORT_INFO</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Include all import information.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_PE_IMAGE_DIGEST_DEBUG_INFO"></a><a id="cert_pe_image_digest_debug_info"></a><dl>
<dt><b>CERT_PE_IMAGE_DIGEST_DEBUG_INFO</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Include symbolic debugging information.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_PE_IMAGE_DIGEST_RESOURCES"></a><a id="cert_pe_image_digest_resources"></a><dl>
<dt><b>CERT_PE_IMAGE_DIGEST_RESOURCES</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Include resource information.

</td>
</tr>
</table>

### -param DigestFunction [in]

A pointer to a callback routine to process the data. For more information, see 
<a href="/windows/desktop/api/imagehlp/nc-imagehlp-digest_function">DigestFunction</a>.

### -param DigestHandle [in]

 A user-supplied handle to the digest. This parameter is passed to <a href="/windows/desktop/api/imagehlp/nc-imagehlp-digest_function">DigestFunction</a> as the first argument.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>ImageGetDigestStream</b> function returns the data to be digested from a specified image file, subject to the passed <i>DigestLevel</i> parameter. The order of the bytes will be consistent for different calls, which is required to ensure that the same message digest is always produced from the retrieved byte stream.

To ensure cross-platform compatibility, all implementations of this function must behave in a consistent manner with respect to the order in which the various parts of the image file are returned.

Data should be returned in the following order:

<ol>
<li>Image (executable and static data) information.</li>
<li>Resource data.</li>
<li>Debugging information.</li>
</ol>
If any of these are not specified, the remaining parts must be returned in the same order.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>