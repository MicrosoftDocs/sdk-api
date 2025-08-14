---
UID: NF:vfw.mmioFOURCC
title: mmioFOURCC macro (vfw.h)
description: The mmioFOURCC macro converts four characters into a four-character code.
helpviewer_keywords: ["_win32_mmioFOURCC","mmioFOURCC","mmioFOURCC macro [Windows Multimedia]","multimedia.mmiofourcc","vfw/mmioFOURCC"]
old-location: multimedia\mmiofourcc.htm
tech.root: Multimedia
ms.assetid: 616c3b43-9305-49c1-bc46-2e1256647c7d
ms.date: 07/01/2025
ms.keywords: _win32_mmioFOURCC, mmioFOURCC, mmioFOURCC macro [Windows Multimedia], multimedia.mmiofourcc, vfw/mmioFOURCC
req.header: vfw.h
req.include-header: Windows.h
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
 - mmioFOURCC
 - vfw/mmioFOURCC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - vfw.h
api_name:
 - mmioFOURCC
---

# mmioFOURCC macro

## -syntax

```cpp
FOURCC mmioFOURCC(
    CHAR ch0,
    CHAR ch1,
    CHAR ch2,
    CHAR ch3
);
```

## -returns

Type: **FOURCC**

Returns the four-character code created from the given characters.


## -description

The <b>mmioFOURCC</b> macro converts four characters into a four-character code.

## -parameters

### -param ch0

First character of the four-character code.

### -param ch1

Second character of the four-character code.

### -param ch2

Third character of the four-character code.

### -param ch3

Fourth character of the four-character code.

## -remarks

This macro does not check whether the four-character code it returns is valid.

The <b>mmioFOURCC</b> macro is defined as follows:


```cpp

#define mmioFOURCC(ch0, ch1, ch2, ch3) \ 
    MAKEFOURCC(ch0, ch1, ch2, ch3); 
 

```


The <b>MAKEFOURCC</b> macro, in turn, is defined as follows:


```cpp

#define MAKEFOURCC(ch0, ch1, ch2, ch3)  \ 
    ((DWORD)(BYTE)(ch0) | ((DWORD)(BYTE)(ch1) << 8) |  \ 
    ((DWORD)(BYTE)(ch2) << 16) | ((DWORD)(BYTE)(ch3) << 24 )); 

```

