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

# ICSeqCompressFrameStart function


## -description



The <b>ICSeqCompressFrameStart</b> function initializes resources for compressing a sequence of frames using the <a href="https://msdn.microsoft.com/6159e455-1e1a-4aa5-9d75-53cd2af2656a">ICSeqCompressFrame</a> function.




## -parameters




### -param pc

Pointer to a <a href="https://msdn.microsoft.com/b34378cb-ccf0-4d97-a952-1966999e3f65">COMPVARS</a> structure initialized with information for compression.


### -param lpbiIn

Format of the data to be compressed.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -remarks



This function uses a <a href="https://msdn.microsoft.com/b34378cb-ccf0-4d97-a952-1966999e3f65">COMPVARS</a> structure to provide settings for the specified compressor and intersperses key frames at the rate specified by the <b>lKey</b> member of <b>COMPVARS</b>. You can specify values for the data rate for the sequence and the key-frame frequency by using the appropriate members of <b>COMPVARS</b>.

Use the <b>ICSeqCompressFrameStart</b>, <a href="https://msdn.microsoft.com/6159e455-1e1a-4aa5-9d75-53cd2af2656a">ICSeqCompressFrame</a>, and <a href="https://msdn.microsoft.com/3fdcd18d-4ee7-4b5a-871d-61316c716e06">ICSeqCompressFrameEnd</a> functions to compress a sequence of frames to a specified data rate and number of key frames.

When finished with compression, use the <a href="https://msdn.microsoft.com/6d0c9a7d-6458-4330-af74-3f471555cbfc">ICCompressorFree</a> function to release the resources specified in <a href="https://msdn.microsoft.com/b34378cb-ccf0-4d97-a952-1966999e3f65">COMPVARS</a>.


<a href="https://msdn.microsoft.com/b34378cb-ccf0-4d97-a952-1966999e3f65">COMPVARS</a> needs to be initialized before you use this function. You can initialize the structure manually or you can allow the user to specify a compressor and initialize a <b>COMPVARS</b> structure by using the <a href="https://msdn.microsoft.com/4a58df6a-9ac4-44bb-8c49-338bb60193fc">ICCompressorChoose</a> function.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

