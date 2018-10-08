---
UID: NF:imagehlp.ImageAddCertificate
title: ImageAddCertificate function
author: windows-sdk-content
description: Adds a certificate to the specified file.
old-location: base\imageaddcertificate.htm
tech.root: debug
ms.assetid: c0cf3845-749b-4d20-ab67-6ace2ac30793
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: ImageAddCertificate, ImageAddCertificate function, _win32_imageaddcertificate, base.imageaddcertificate, imagehlp/ImageAddCertificate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imagehlp.dll
api_name:
 - ImageAddCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The certificate is added at the end of the existing list of certificates and is assigned an index.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/926f412e-25ba-4f9c-a118-b5a1bc723379">ImageHlp Functions</a>



<a href="https://msdn.microsoft.com/e06da4c5-6641-47f8-9dd9-4a1593e11f7b">ImageRemoveCertificate</a>
 

 

