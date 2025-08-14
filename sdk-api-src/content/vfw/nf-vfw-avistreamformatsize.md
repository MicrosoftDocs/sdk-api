---
UID: NF:vfw.AVIStreamFormatSize
title: AVIStreamFormatSize macro (vfw.h)
description: The AVIStreamFormatSize macro determines the buffer size, in bytes, needed to store format information for a sample in a stream.
helpviewer_keywords: ["AVIStreamFormatSize","AVIStreamFormatSize macro [Windows Multimedia]","_win32_AVIStreamFormatSize","multimedia.avistreamformatsize","vfw/AVIStreamFormatSize"]
old-location: multimedia\avistreamformatsize.htm
tech.root: Multimedia
ms.assetid: e29bbbc3-28b2-44d3-b1f1-66ad2b29a7a3
ms.date: 07/01/2025
ms.keywords: AVIStreamFormatSize, AVIStreamFormatSize macro [Windows Multimedia], _win32_AVIStreamFormatSize, multimedia.avistreamformatsize, vfw/AVIStreamFormatSize
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
 - AVIStreamFormatSize
 - vfw/AVIStreamFormatSize
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
 - AVIStreamFormatSize
---

# AVIStreamFormatSize macro

## -syntax

```cpp
HRESULT AVIStreamFormatSize(
     pavi,
     lPos,
     plSize
);
```

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

Returns zero if successful or an error otherwise.


## -description

The <b>AVIStreamFormatSize</b> macro determines the buffer size, in bytes, needed to store format information for a sample in a stream.

## -parameters

### -param pavi

Handle to an open stream.

### -param lPos

Position of a sample in the stream.

### -param plSize

Address to contain the buffer size.

## -remarks

The <b>AVIStreamFormatSize</b> macro is defined as follows:


```cpp

#define AVIStreamFormatSize(pavi, lPos, plSize) \ 
    AVIStreamReadFormat(pavi, lPos, NULL, plSize) 

```

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
