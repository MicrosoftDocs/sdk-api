---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

