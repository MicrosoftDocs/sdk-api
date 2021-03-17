---
UID: NF:imagehlp.ImageGetCertificateHeader
title: ImageGetCertificateHeader function (imagehlp.h)
description: Retrieves the header of the specified certificate, up to, but not including, the section offset array.
helpviewer_keywords: ["ImageGetCertificateHeader","ImageGetCertificateHeader function","_win32_imagegetcertificateheader","base.imagegetcertificateheader","imagehlp/ImageGetCertificateHeader"]
old-location: base\imagegetcertificateheader.htm
tech.root: Debug
ms.assetid: 84b10926-7f49-406c-8939-d85f62844806
ms.date: 12/05/2018
ms.keywords: ImageGetCertificateHeader, ImageGetCertificateHeader function, _win32_imagegetcertificateheader, base.imagegetcertificateheader, imagehlp/ImageGetCertificateHeader
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
 - ImageGetCertificateHeader
 - imagehlp/ImageGetCertificateHeader
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
 - ImageGetCertificateHeader
---

# ImageGetCertificateHeader function


## -description

Retrieves the header of the specified certificate, up to, but not including, the section offset array.

## -parameters

### -param FileHandle [in]

A handle to the image file. This handle must be opened for FILE_READ_DATA access.

### -param CertificateIndex [in]

The index of the certificate whose header is to be returned.

### -param Certificateheader [in, out]

A pointer to the <b>WIN_CERTIFICATE</b> structure that receives the certificate header.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>