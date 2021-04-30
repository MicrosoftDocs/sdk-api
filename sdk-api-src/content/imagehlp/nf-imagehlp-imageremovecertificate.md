---
UID: NF:imagehlp.ImageRemoveCertificate
title: ImageRemoveCertificate function (imagehlp.h)
description: Removes the specified certificate from the given file.
helpviewer_keywords: ["ImageRemoveCertificate","ImageRemoveCertificate function","_win32_imageremovecertificate","base.imageremovecertificate","imagehlp/ImageRemoveCertificate"]
old-location: base\imageremovecertificate.htm
tech.root: Debug
ms.assetid: e06da4c5-6641-47f8-9dd9-4a1593e11f7b
ms.date: 12/05/2018
ms.keywords: ImageRemoveCertificate, ImageRemoveCertificate function, _win32_imageremovecertificate, base.imageremovecertificate, imagehlp/ImageRemoveCertificate
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
 - ImageRemoveCertificate
 - imagehlp/ImageRemoveCertificate
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
 - ImageRemoveCertificate
---

# ImageRemoveCertificate function


## -description

Removes the specified certificate from the given file.

## -parameters

### -param FileHandle [in]

A handle to the image file to be modified. This handle must be opened for FILE_READ_DATA and FILE_WRITE_DATA access.

### -param Index [in]

The index of the certificate to be removed.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imageaddcertificate">ImageAddCertificate</a>



<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>