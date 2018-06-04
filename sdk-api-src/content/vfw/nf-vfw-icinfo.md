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

# ICInfo function


## -description



The <b>ICInfo</b> function retrieves information about specific installed compressors or enumerates the installed compressors.




## -parameters




### -param fccType

Four-character code indicating the type of compressor. Specify zero to match all compressor types.


### -param fccHandler

Four-character code identifying a specific compressor or a number between zero and the number of installed compressors of the type specified by <i>fccType</i>.


### -param lpicinfo

Pointer to a <a href="https://msdn.microsoft.com/5faf7022-6dc8-475c-8f5a-721bc5b6afee">ICINFO</a> structure to return information about the compressor.


## -returns



Returns <b>TRUE</b> if successful or an error otherwise.




## -remarks



To enumerate the compressors or decompressors, specify an integer for <i>fccHandler</i>. This function returns information for integers between zero and the number of installed compressors or decompressors of the type specified for <i>fccType</i>.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

