---
UID: NF:imagehlp.ImageGetCertificateData
title: ImageGetCertificateData function (imagehlp.h)
description: Retrieves a complete certificate from a file.
helpviewer_keywords: ["ImageGetCertificateData","ImageGetCertificateData function","_win32_imagegetcertificatedata","base.imagegetcertificatedata","imagehlp/ImageGetCertificateData"]
old-location: base\imagegetcertificatedata.htm
tech.root: Debug
ms.assetid: ca4cf3a3-9324-4784-a6d8-44692f4840eb
ms.date: 12/05/2018
ms.keywords: ImageGetCertificateData, ImageGetCertificateData function, _win32_imagegetcertificatedata, base.imagegetcertificatedata, imagehlp/ImageGetCertificateData
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
 - ImageGetCertificateData
 - imagehlp/ImageGetCertificateData
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
 - ImageGetCertificateData
---

# ImageGetCertificateData function


## -description

Retrieves a complete certificate from a file.

## -parameters

### -param FileHandle [in]

A handle to the image file. This handle must be opened for <b>FILE_READ_DATA</b> access.

### -param CertificateIndex [in]

The index of the certificate to be returned.

### -param Certificate [out]

A pointer to a <b>WIN_CERTIFICATE</b> structure that receives the certificate data. If the buffer is not large enough to contain the structure, the function fails and the last error code is set to <b>ERROR_INSUFFICIENT_BUFFER</b>.

### -param RequiredLength [in, out]

On input, this parameter specifies the length of the <i>Certificate</i> buffer in bytes. On success, it receives the length of the certificate.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The    <b>WIN_CERTIFICATE</b> structure is defined as follows: 


```cpp
typedef struct _WIN_CERTIFICATE {
    DWORD       dwLength;
    WORD        wRevision;
    WORD        wCertificateType;   // WIN_CERT_TYPE_xxx
    BYTE        bCertificate[ANYSIZE_ARRAY];
} WIN_CERTIFICATE, *LPWIN_CERTIFICATE;
```


All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>