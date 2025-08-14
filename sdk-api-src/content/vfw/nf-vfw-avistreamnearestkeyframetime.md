---
UID: NF:vfw.AVIStreamNearestKeyFrameTime
title: AVIStreamNearestKeyFrameTime macro (vfw.h)
description: The AVIStreamNearestKeyFrameTime macro determines the time corresponding to the beginning of the key frame nearest (at or preceding) a specified time in a stream.
helpviewer_keywords: ["AVIStreamNearestKeyFrameTime","AVIStreamNearestKeyFrameTime macro [Windows Multimedia]","_win32_AVIStreamNearestKeyFrameTime","multimedia.avistreamnearestkeyframetime","vfw/AVIStreamNearestKeyFrameTime"]
old-location: multimedia\avistreamnearestkeyframetime.htm
tech.root: Multimedia
ms.assetid: 7409e8e3-d151-4970-9c0e-84ecdf9846a0
ms.date: 07/01/2025
ms.keywords: AVIStreamNearestKeyFrameTime, AVIStreamNearestKeyFrameTime macro [Windows Multimedia], _win32_AVIStreamNearestKeyFrameTime, multimedia.avistreamnearestkeyframetime, vfw/AVIStreamNearestKeyFrameTime
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVIStreamNearestKeyFrameTime
 - vfw/AVIStreamNearestKeyFrameTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - AVIStreamNearestKeyFrameTime
---

# AVIStreamNearestKeyFrameTime macro

## -syntax

```cpp
LONG AVIStreamNearestKeyFrameTime(
     pavi,
     t
);
```

## -returns

Type: **LONG**

Returns the time of the nearest key frame if successful or –1 otherwise.


## -description

The <b>AVIStreamNearestKeyFrameTime</b> macro determines the time corresponding to the beginning of the key frame nearest (at or preceding) a specified time in a stream.

## -parameters

### -param pavi

Handle to an open stream.

### -param t

Starting time, in milliseconds, to search in the stream.

## -remarks

The <b>AVIStreamNearestKeyFrameTime</b> macro is defined as follows:


```cpp

#define AVIStreamNearestKeyFrameTime(pavi, t) \ 
    AVIStreamSampleToTime(pavi, AVIStreamNearestKeyFrame(pavi, 
    AVIStreamTimeToSample(pavi, t))) 

```

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
