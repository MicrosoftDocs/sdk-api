---
UID: NF:imagehlp.ImageEnumerateCertificates
title: ImageEnumerateCertificates function (imagehlp.h)
description: Retrieves information about the certificates currently contained in an image file.
helpviewer_keywords: ["ImageEnumerateCertificates","ImageEnumerateCertificates function","_win32_imageenumeratecertificates","base.imageenumeratecertificates","imagehlp/ImageEnumerateCertificates"]
old-location: base\imageenumeratecertificates.htm
tech.root: Debug
ms.assetid: 5f2e4fb7-180a-4172-9c38-5f65dfd29f69
ms.date: 12/05/2018
ms.keywords: ImageEnumerateCertificates, ImageEnumerateCertificates function, _win32_imageenumeratecertificates, base.imageenumeratecertificates, imagehlp/ImageEnumerateCertificates
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
 - ImageEnumerateCertificates
 - imagehlp/ImageEnumerateCertificates
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
 - ImageEnumerateCertificates
---

# ImageEnumerateCertificates function


## -description

Retrieves information about the certificates currently contained in an image file.

## -parameters

### -param FileHandle [in]

A handle to the image file to be examined. This handle must be opened for FILE_READ_DATA access.

### -param TypeFilter [in]

The certificate section type to be used as a filter when returning certificate information. CERT_SECTION_TYPE_ANY should be passed for information on all section types present in the image.

### -param CertificateCount [out]

A pointer to a variable that receives the number of certificates in the image containing sections of the type specified by the <i>TypeFilter</i> parameter. If none are found, this parameter is zero.

### -param Indices [in, out]

Optionally provides a buffer to use to return an array of indices to the certificates containing sections of the specified type. No ordering should be assumed for the index values, nor are they guaranteed to be contiguous when CERT_SECTION_TYPE_ANY is queried.

### -param IndexCount [in, optional]

The size of the <i>Indices</i> buffer, in <b>DWORDs</b>. This parameter will be examined whenever <i>Indices</i> is present. If <i>CertificateCount</i> is greater than <i>IndexCount</i>, <i>Indices</i> will be filled in with the first <i>IndexCount</i> sections found in the image; any others will not be returned.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>ImageEnumerateCertificates</b> function returns information about the certificates currently contained in an image file. It has filtering capabilities which allow certificates containing sections of any single type (or of any type) to be returned.

After the indices of interesting certificates are discovered, they can be passed to the 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imagegetcertificatedata">ImageGetCertificateData</a> function to obtain the actual bodies of the certificates.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imagegetcertificatedata">ImageGetCertificateData</a>



<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>