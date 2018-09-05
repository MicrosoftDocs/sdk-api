---
UID: NC:imagehlp.DIGEST_FUNCTION
title: DIGEST_FUNCTION
author: windows-sdk-content
description: An application-defined callback function used by the ImageGetDigestStream function to process data.
old-location: base\digestfunction.htm
old-project: debug
ms.assetid: 4d5d2593-d9e2-43e8-914b-11f578192085
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: DIGEST_FUNCTION, DigestFunction, DigestFunction callback, DigestFunction callback function, _win32_digestfunction, base.digestfunction, imagehlp/DigestFunction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: imagehlp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Imagehlp.h
api_name:
 - DigestFunction
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# DIGEST_FUNCTION callback function


## -description


An application-defined callback function used by the 
<a href="https://msdn.microsoft.com/e4560609-5b10-453f-a9a6-c5483d88cd64">ImageGetDigestStream</a> function to process data.

The <b>DIGEST_FUNCTION</b> type defines a pointer to this callback function. 
<b>DigestFunction</b> is a placeholder for the application-defined function name.


## -parameters




### -param refdata [in]

A user-supplied handle to the digest. This value is passed as a parameter to the 
<a href="https://msdn.microsoft.com/e4560609-5b10-453f-a9a6-c5483d88cd64">ImageGetDigestStream</a> function.


### -param pData [in]

The data stream.


### -param dwLength [in]

The size of the data stream, in bytes.


## -returns



If the function succeeds, the return value should be <b>TRUE</b>. If the function fails, the return value should be <b>FALSE</b>.




## -remarks



All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/e4560609-5b10-453f-a9a6-c5483d88cd64">ImageGetDigestStream</a>



<a href="https://msdn.microsoft.com/926f412e-25ba-4f9c-a118-b5a1bc723379">ImageHlp Functions</a>
 

 

