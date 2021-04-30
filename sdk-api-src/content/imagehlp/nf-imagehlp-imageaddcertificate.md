---
UID: NF:imagehlp.ImageAddCertificate
title: ImageAddCertificate function (imagehlp.h)
description: Adds a certificate to the specified file.
helpviewer_keywords: ["ImageAddCertificate","ImageAddCertificate function","_win32_imageaddcertificate","base.imageaddcertificate","imagehlp/ImageAddCertificate"]
old-location: base\imageaddcertificate.htm
tech.root: Debug
ms.assetid: c0cf3845-749b-4d20-ab67-6ace2ac30793
ms.date: 12/05/2018
ms.keywords: ImageAddCertificate, ImageAddCertificate function, _win32_imageaddcertificate, base.imageaddcertificate, imagehlp/ImageAddCertificate
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
 - ImageAddCertificate
 - imagehlp/ImageAddCertificate
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
 - ImageAddCertificate
---

# ImageAddCertificate function


## -description

Adds a certificate to the specified file.

## -parameters

### -param FileHandle [in]

A handle to the image file to be modified. This handle must be opened for FILE_READ_DATA and FILE_WRITE_DATA access.

### -param Certificate [in]

A pointer to a <b>WIN_CERTIFICATE</b> header and all associated sections. The <b>Length</b> member in the certificate header will be used to determine the length of this buffer.

### -param Index [out]

A pointer to a variable that receives the index of the newly added certificate.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The certificate is added at the end of the existing list of certificates and is assigned an index.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>



<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imageremovecertificate">ImageRemoveCertificate</a>