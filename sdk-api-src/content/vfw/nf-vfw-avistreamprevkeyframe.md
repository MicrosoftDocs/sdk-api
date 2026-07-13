---
UID: NF:vfw.AVIStreamPrevKeyFrame
title: AVIStreamPrevKeyFrame macro (vfw.h)
description: The AVIStreamPrevKeyFrame macro locates the key frame that precedes a specified position in a stream.
helpviewer_keywords: ["AVIStreamPrevKeyFrame","AVIStreamPrevKeyFrame macro [Windows Multimedia]","_win32_AVIStreamPrevKeyFrame","multimedia.avistreamprevkeyframe","vfw/AVIStreamPrevKeyFrame"]
old-location: multimedia\avistreamprevkeyframe.htm
tech.root: Multimedia
ms.assetid: 69933c8f-7e4e-45b2-aa72-ac127f3c8d05
ms.date: 07/01/2025
ms.keywords: AVIStreamPrevKeyFrame, AVIStreamPrevKeyFrame macro [Windows Multimedia], _win32_AVIStreamPrevKeyFrame, multimedia.avistreamprevkeyframe, vfw/AVIStreamPrevKeyFrame
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
 - AVIStreamPrevKeyFrame
 - vfw/AVIStreamPrevKeyFrame
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
 - AVIStreamPrevKeyFrame
---

# AVIStreamPrevKeyFrame macro

## -syntax

```cpp
LONG AVIStreamPrevKeyFrame(
     pavi,
     l
);
```

## -returns

Type: **LONG**

Returns the position of the key frame if successful or –1 otherwise.


## -description

The <b>AVIStreamPrevKeyFrame</b> macro locates the key frame that precedes a specified position in a stream.

## -parameters

### -param pavi

Handle to an open stream.

### -param l

Starting position to search in the stream.

## -remarks

The search performed by this macro does not include the frame at the specified position.

The <b>AVIStreamPrevKeyFrame</b> macro is defined as follows:


```cpp

#define AVIStreamPrevKeyFrame(pavi, l) \ 
    AVIStreamFindSample(pavi, l - 1, FIND_PREV | FIND_KEY) 

```

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
