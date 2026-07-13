---
UID: NF:vfw.AVIStreamEndTime
title: AVIStreamEndTime macro (vfw.h)
description: The AVIStreamEndTime macro returns the time representing the end of the stream.
helpviewer_keywords: ["AVIStreamEndTime","AVIStreamEndTime macro [Windows Multimedia]","_win32_AVIStreamEndTime","multimedia.avistreamendtime","vfw/AVIStreamEndTime"]
old-location: multimedia\avistreamendtime.htm
tech.root: Multimedia
ms.assetid: 0fd3c0c7-34cc-4193-8e6a-9866a9d651a2
ms.date: 07/01/2025
ms.keywords: AVIStreamEndTime, AVIStreamEndTime macro [Windows Multimedia], _win32_AVIStreamEndTime, multimedia.avistreamendtime, vfw/AVIStreamEndTime
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
 - AVIStreamEndTime
 - vfw/AVIStreamEndTime
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
 - AVIStreamEndTime
---

# AVIStreamEndTime macro

## -syntax

```cpp
LONG AVIStreamEndTime(
     pavi
);
```

## -returns

Type: **LONG**

Returns the time if successful or -1 otherwise.


## -description

The <b>AVIStreamEndTime</b> macro returns the time representing the end of the stream.

## -parameters

### -param pavi

Handle to an open stream.

## -remarks

The <b>AVIStreamEndTime</b> macro is defined as follows:


```cpp

#define AVIStreamEndTime(pavi) \ 
    AVIStreamSampleToTime(pavi, AVIStreamEnd(pavi)) 

```

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
