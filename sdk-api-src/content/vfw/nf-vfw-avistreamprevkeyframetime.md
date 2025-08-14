---
UID: NF:vfw.AVIStreamPrevKeyFrameTime
title: AVIStreamPrevKeyFrameTime macro (vfw.h)
description: The AVIStreamPrevKeyFrameTime macro returns the time of the previous key frame in the stream, starting at a given time.
helpviewer_keywords: ["AVIStreamPrevKeyFrameTime","AVIStreamPrevKeyFrameTime macro [Windows Multimedia]","_win32_AVIStreamPrevKeyFrameTime","multimedia.avistreamprevkeyframetime","vfw/AVIStreamPrevKeyFrameTime"]
old-location: multimedia\avistreamprevkeyframetime.htm
tech.root: Multimedia
ms.assetid: 0da49be2-b017-4d41-b9da-3c1310fa0289
ms.date: 07/01/2025
ms.keywords: AVIStreamPrevKeyFrameTime, AVIStreamPrevKeyFrameTime macro [Windows Multimedia], _win32_AVIStreamPrevKeyFrameTime, multimedia.avistreamprevkeyframetime, vfw/AVIStreamPrevKeyFrameTime
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
 - AVIStreamPrevKeyFrameTime
 - vfw/AVIStreamPrevKeyFrameTime
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
 - AVIStreamPrevKeyFrameTime
---

# AVIStreamPrevKeyFrameTime macro

## -syntax

```cpp
LONG AVIStreamPrevKeyFrameTime(
     pavi,
     t
);
```

## -returns

Type: **LONG**

Returns the time if successful or –1 otherwise.


## -description

The <b>AVIStreamPrevKeyFrameTime</b> macro returns the time of the previous key frame in the stream, starting at a given time.

## -parameters

### -param pavi

Handle to an open stream.

### -param t

Position in the stream to begin searching.

## -remarks

The search performed by this macro includes the frame that corresponds to the specified time.

The <b>AVIStreamPrevKeyFrameTime</b> macro is defined as follows:


```cpp

#define AVIStreamPrevKeyFrameTime(pavi, t) \ 
    AVIStreamSampleToTime(pavi, AVIStreamPrevKeyFrame(pavi, 
    AVIStreamTimeToSample(pavi, t))) 

```

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
