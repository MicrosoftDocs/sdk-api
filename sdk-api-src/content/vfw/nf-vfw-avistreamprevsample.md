---
UID: NF:vfw.AVIStreamPrevSample
title: AVIStreamPrevSample macro (vfw.h)
description: The AVIStreamPrevSample macro locates the nearest nonempty sample that precedes a specified position in a stream.
helpviewer_keywords: ["AVIStreamPrevSample","AVIStreamPrevSample macro [Windows Multimedia]","_win32_AVIStreamPrevSample","multimedia.avistreamprevsample","vfw/AVIStreamPrevSample"]
old-location: multimedia\avistreamprevsample.htm
tech.root: Multimedia
ms.assetid: 86bc141f-6e58-49ac-b3f1-1e29e028be31
ms.date: 07/01/2025
ms.keywords: AVIStreamPrevSample, AVIStreamPrevSample macro [Windows Multimedia], _win32_AVIStreamPrevSample, multimedia.avistreamprevsample, vfw/AVIStreamPrevSample
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
 - AVIStreamPrevSample
 - vfw/AVIStreamPrevSample
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
 - AVIStreamPrevSample
---

# AVIStreamPrevSample macro

## -syntax

```cpp
LONG AVIStreamPrevSample(
     pavi,
     l
);
```

## -returns

Type: **LONG**

Returns the sample position if successful or –1 otherwise.


## -description

The <b>AVIStreamPrevSample</b> macro locates the nearest nonempty sample that precedes a specified position in a stream.

## -parameters

### -param pavi

Handle to an open stream.

### -param l

Starting position to search in the stream.

## -remarks

The sample position returned does not include the sample specified by <i>l</i>.

The <b>AVIStreamPrevSample</b> macro is defined as follows:


```cpp

#define AVIStreamPrevSample(pavi, l) \ 
    AVIStreamFindSample(pavi, l - 1, FIND_PREV | FIND_ANY) 

```

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
