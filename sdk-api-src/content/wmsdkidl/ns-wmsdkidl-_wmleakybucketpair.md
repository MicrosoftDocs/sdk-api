---
UID: NS:wmsdkidl._WMLeakyBucketPair
title: "_WMLeakyBucketPair"
author: windows-sdk-content
description: The WM_LEAKY_BUCKET_PAIR structure describes the buffering requirements for a VBR file. This structure is used with the ASFLeakyBucketPairs attribute.
old-location: wmformat\wm_leaky_bucket_pair.htm
tech.root: wmformat
ms.assetid: 8fada83d-cb66-4411-9ff5-0eb4c02a3b5f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WM_LEAKY_BUCKET_PAIR, WM_LEAKY_BUCKET_PAIR structure [windows Media Format], _WMLeakyBucketPair, wmformat.wm_leaky_bucket_pair, wmsdkidl/WM_LEAKY_BUCKET_PAIR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WM_LEAKY_BUCKET_PAIR
product: Windows
targetos: Windows
req.typenames: WM_LEAKY_BUCKET_PAIR
req.redist: 
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




<a href="https://msdn.microsoft.com/118ef278-ca4f-4c30-9633-a2d851f5c758">Structures</a>
 

 

