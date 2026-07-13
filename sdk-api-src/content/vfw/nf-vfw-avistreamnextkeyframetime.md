---
UID: NF:vfw.AVIStreamNextKeyFrameTime
title: AVIStreamNextKeyFrameTime macro (vfw.h)
description: The AVIStreamNextKeyFrameTime macro returns the time of the next key frame in the stream, starting at a given time.
helpviewer_keywords: ["AVIStreamNextKeyFrameTime","AVIStreamNextKeyFrameTime macro [Windows Multimedia]","_win32_AVIStreamNextKeyFrameTime","multimedia.avistreamnextkeyframetime","vfw/AVIStreamNextKeyFrameTime"]
old-location: multimedia\avistreamnextkeyframetime.htm
tech.root: Multimedia
ms.assetid: 5eb338aa-6ccb-4adc-a46c-9f796c36a121
ms.date: 07/01/2025
ms.keywords: AVIStreamNextKeyFrameTime, AVIStreamNextKeyFrameTime macro [Windows Multimedia], _win32_AVIStreamNextKeyFrameTime, multimedia.avistreamnextkeyframetime, vfw/AVIStreamNextKeyFrameTime
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
 - AVIStreamNextKeyFrameTime
 - vfw/AVIStreamNextKeyFrameTime
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
 - AVIStreamNextKeyFrameTime
---

# AVIStreamNextKeyFrameTime macro

## -syntax

```cpp
LONG AVIStreamNextKeyFrameTime(
     pavi,
     t
);
```

## -returns

Type: **LONG**

Returns the time if successful or –1 otherwise.


## -description

The <b>AVIStreamNextKeyFrameTime</b> macro returns the time of the next key frame in the stream, starting at a given time.

## -parameters

### -param pavi

Handle to an open stream.

### -param t

Position in the stream to begin searching.

## -remarks

The search performed by this macro includes the frame that corresponds to the specified time.

The <b>AVIStreamNextKeyFrameTime</b> macro is defined as follows:


```cpp

#define AVIStreamNextKeyFrameTime(pavi, t) \ 
    AVIStreamSampleToTime(pavi, \ 
    AVIStreamNextKeyFrame(pavi, \ 
    AVIStreamTimeToSample(pavi, t))) 

```

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
