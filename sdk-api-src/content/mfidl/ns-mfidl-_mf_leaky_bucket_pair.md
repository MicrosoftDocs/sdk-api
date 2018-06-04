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

# _MF_LEAKY_BUCKET_PAIR structure


## -description



Specifies the buffering requirements of a file.




## -struct-fields




### -field dwBitrate

Bit rate, in bits per second.


### -field msBufferWindow

Size of the buffer window, in milliseconds.


## -remarks



This structure describes the buffering requirements for content encoded at the bit rate specified in the <b>dwBitrate</b>. The <b>msBufferWindow</b> member indicates how much data should be buffered before starting playback. The size of the buffer in bytes is <b>msBufferWinow</b>×<b>dwBitrate</b> / 8000.




## -see-also




<a href="https://msdn.microsoft.com/6667d32c-36a8-414e-a546-02d00a447b70">MFBYTESTREAM_BUFFERING_PARAMS</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

