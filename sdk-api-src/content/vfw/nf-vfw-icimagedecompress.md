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

# ICImageDecompress function


## -description



The <b>ICImageDecompress</b> function decompresses an image without using initialization functions.




## -parameters




### -param hic

Handle to a decompressor opened with the <a href="https://msdn.microsoft.com/2637b6ef-2324-40db-99e4-773fcb6fdbf6">ICOpen</a> function. Specify <b>NULL</b> to have VCM select an appropriate decompressor for the compressed image.


### -param uiFlags

Reserved; must be zero.


### -param lpbiIn

Compressed input data format.


### -param lpBits

Pointer to input data bits to compress. The data bits exclude header and format information.


### -param lpbiOut

Decompressed output format. Specify <b>NULL</b> to let decompressor use an appropriate format.


## -returns



Returns a handle to an uncompressed DIB in the CF_DIB format if successful or <b>NULL</b> otherwise. Image data follows the format header.




## -remarks



To obtain the format information from the <b>LPBITMAPINFOHEADER</b> structure, use the <b>GlobalLock</b> function to lock the data. Use the <b>GlobalFree</b> function to free the DIB when you are finished.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

