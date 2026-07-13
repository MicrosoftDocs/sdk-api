---
UID: NF:vfw.AVIStreamNextKeyFrame
title: AVIStreamNextKeyFrame macro (vfw.h)
description: The AVIStreamNextKeyFrame macro locates the next key frame following a specified position in a stream.
helpviewer_keywords: ["AVIStreamNextKeyFrame","AVIStreamNextKeyFrame macro [Windows Multimedia]","_win32_AVIStreamNextKeyFrame","multimedia.avistreamnextkeyframe","vfw/AVIStreamNextKeyFrame"]
old-location: multimedia\avistreamnextkeyframe.htm
tech.root: Multimedia
ms.assetid: 928b5deb-2f68-4fed-98cf-8130379c8622
ms.date: 07/01/2025
ms.keywords: AVIStreamNextKeyFrame, AVIStreamNextKeyFrame macro [Windows Multimedia], _win32_AVIStreamNextKeyFrame, multimedia.avistreamnextkeyframe, vfw/AVIStreamNextKeyFrame
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
 - AVIStreamNextKeyFrame
 - vfw/AVIStreamNextKeyFrame
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
 - AVIStreamNextKeyFrame
---

# AVIStreamNextKeyFrame macro

## -syntax

```cpp
LONG AVIStreamNextKeyFrame(
     pavi,
     l
);
```

## -returns

Type: **LONG**

Returns the position of the key frame if successful or –1 otherwise.


## -description

The <b>AVIStreamNextKeyFrame</b> macro locates the next key frame following a specified position in a stream.

## -parameters

### -param pavi

Handle to an open stream.

### -param l

Starting position to search in the stream.

## -remarks

The search performed by this macro does not include the frame at the specified position.

The <b>AVIStreamNextKeyFrame</b> macro is defined as follows:


```cpp

#define AVIStreamNextKeyFrame(pavi, l) \ 
    AVIStreamFindSample(pavi, l + 1, FIND_NEXT | FIND_KEY) 

```

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
