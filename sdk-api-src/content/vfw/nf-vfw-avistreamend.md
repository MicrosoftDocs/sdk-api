---
UID: NF:vfw.AVIStreamEnd
title: AVIStreamEnd macro (vfw.h)
description: The AVIStreamEnd macro calculates the sample associated with the end of a stream.
helpviewer_keywords: ["AVIStreamEnd","AVIStreamEnd macro [Windows Multimedia]","_win32_AVIStreamEnd","multimedia.avistreamend","vfw/AVIStreamEnd"]
old-location: multimedia\avistreamend.htm
tech.root: Multimedia
ms.assetid: 9c132953-1b24-4a5f-b2e9-b5569a579696
ms.date: 07/01/2025
ms.keywords: AVIStreamEnd, AVIStreamEnd macro [Windows Multimedia], _win32_AVIStreamEnd, multimedia.avistreamend, vfw/AVIStreamEnd
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
 - AVIStreamEnd
 - vfw/AVIStreamEnd
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
 - AVIStreamEnd
---

# AVIStreamEnd macro

## -syntax

```cpp
LONG AVIStreamEnd(
     pavi
);
```

## -returns

Type: **LONG**

Returns the sample number associated with the end of a stream, or, if an error occurs, one less than the first sample or one less than the stream length.


## -description

The <b>AVIStreamEnd</b> macro calculates the sample associated with the end of a stream.

## -parameters

### -param pavi

Handle to an open stream.

## -remarks

The sample number returned is not a valid sample number for reading data. It represents the end of the file. (The end of the file is equal to the start of the file plus its length.)

The <b>AVIStreamEnd</b> macro is defined as follows:


```cpp

#define AVIStreamEnd(pavi) \ 
    (AVIStreamStart(pavi) + AVIStreamLength(pavi)) 

```

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
