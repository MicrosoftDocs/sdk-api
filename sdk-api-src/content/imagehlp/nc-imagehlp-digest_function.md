---
UID: NC:imagehlp.DIGEST_FUNCTION
title: DIGEST_FUNCTION (imagehlp.h)
description: An application-defined callback function used by the ImageGetDigestStream function to process data.
helpviewer_keywords: ["DIGEST_FUNCTION","DigestFunction","DigestFunction callback","DigestFunction callback function","_win32_digestfunction","base.digestfunction","imagehlp/DigestFunction"]
old-location: base\digestfunction.htm
tech.root: Debug
ms.assetid: 4d5d2593-d9e2-43e8-914b-11f578192085
ms.date: 12/05/2018
ms.keywords: DIGEST_FUNCTION, DigestFunction, DigestFunction callback, DigestFunction callback function, _win32_digestfunction, base.digestfunction, imagehlp/DigestFunction
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DIGEST_FUNCTION
 - imagehlp/DIGEST_FUNCTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Imagehlp.h
api_name:
 - DigestFunction
---

# DIGEST_FUNCTION callback function


## -description

An application-defined callback function used by the 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imagegetdigeststream">ImageGetDigestStream</a> function to process data.

The <b>DIGEST_FUNCTION</b> type defines a pointer to this callback function. 
<b>DigestFunction</b> is a placeholder for the application-defined function name.

## -parameters

### -param refdata [in]

A user-supplied handle to the digest. This value is passed as a parameter to the 
<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imagegetdigeststream">ImageGetDigestStream</a> function.

### -param pData [in]

The data stream.

### -param dwLength [in]

The size of the data stream, in bytes.

## -returns

If the function succeeds, the return value should be <b>TRUE</b>. If the function fails, the return value should be <b>FALSE</b>.

## -remarks

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imagegetdigeststream">ImageGetDigestStream</a>



<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>