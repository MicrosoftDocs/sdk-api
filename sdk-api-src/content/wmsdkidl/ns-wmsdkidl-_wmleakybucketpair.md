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

# _WMLeakyBucketPair structure


## -description



The <b>WM_LEAKY_BUCKET_PAIR </b>structure describes the buffering requirements for a VBR file. This structure is used with the <a href="https://msdn.microsoft.com/d1b3e8cc-c082-4283-88bc-172f58adf2d9">ASFLeakyBucketPairs</a> attribute.




## -struct-fields




### -field dwBitrate

Bit rate, in bits per second.


### -field msBufferWindow

Size of the buffer window, in milliseconds.


## -remarks



The <b>ASFLeakyBucketPairs</b> attribute gives a list of bit rates and corresponding buffer windows. For each bit rate, the <b>msBufferWindow</b> member indicates how much content the reader object will buffer before it begins playback. The size of the buffer in bytes equals <b>msBufferWinow</b> x <b>dwBitrate</b> / 8000.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

