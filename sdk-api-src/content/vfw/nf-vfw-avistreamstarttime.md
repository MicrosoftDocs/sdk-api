---
UID: NF:vfw.AVIStreamStartTime
title: AVIStreamStartTime macro (vfw.h)
description: The AVIStreamStartTime macro returns the starting time of a stream's first sample.
helpviewer_keywords: ["AVIStreamStartTime","AVIStreamStartTime macro [Windows Multimedia]","_win32_AVIStreamStartTime","multimedia.avistreamstarttime","vfw/AVIStreamStartTime"]
old-location: multimedia\avistreamstarttime.htm
tech.root: Multimedia
ms.assetid: 6bfa053f-26ca-4dc8-8896-11ee9f0d9b77
ms.date: 07/01/2025
ms.keywords: AVIStreamStartTime, AVIStreamStartTime macro [Windows Multimedia], _win32_AVIStreamStartTime, multimedia.avistreamstarttime, vfw/AVIStreamStartTime
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
 - AVIStreamStartTime
 - vfw/AVIStreamStartTime
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
 - AVIStreamStartTime
---

# AVIStreamStartTime macro

## -syntax

```cpp
LONG AVIStreamStartTime(
     pavi
);
```

## -returns

Type: **LONG**

Returns the time if successful or –1 otherwise.


## -description

The <b>AVIStreamStartTime</b> macro returns the starting time of a stream's first sample.

## -parameters

### -param pavi

Handle to an open stream.

## -remarks

The <b>AVIStreamStartTime</b> macro is defined as follows:


```cpp

#define AVIStreamStartTime(pavi) \ 
    AVIStreamSampleToTime(pavi, AVIStreamStart(pavi)) 

```

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
