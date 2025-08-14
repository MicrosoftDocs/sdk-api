---
UID: NF:vfw.AVIStreamDataSize
title: AVIStreamDataSize macro (vfw.h)
description: The AVIStreamDataSize macro determines the buffer size, in bytes, needed to retrieve optional header data for a specified stream.
helpviewer_keywords: ["AVIStreamDataSize","AVIStreamDataSize macro [Windows Multimedia]","_win32_AVIStreamDataSize","multimedia.avistreamdatasize","vfw/AVIStreamDataSize"]
old-location: multimedia\avistreamdatasize.htm
tech.root: Multimedia
ms.assetid: e91258ee-b90a-43b9-9d5e-0adee215714c
ms.date: 07/01/2025
ms.keywords: AVIStreamDataSize, AVIStreamDataSize macro [Windows Multimedia], _win32_AVIStreamDataSize, multimedia.avistreamdatasize, vfw/AVIStreamDataSize
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
 - AVIStreamDataSize
 - vfw/AVIStreamDataSize
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
 - AVIStreamDataSize
---

# AVIStreamDataSize macro

## -syntax

```cpp
HRESULT AVIStreamDataSize(
     pavi,
     fcc,
     plSize
);
```

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

Returns zero if successful or an error otherwise. The return value AVIERR_NODATA indicates the system could not find any data with the specified four-character code.


## -description

The <b>AVIStreamDataSize</b> macro determines the buffer size, in bytes, needed to retrieve optional header data for a specified stream.

## -parameters

### -param pavi

Handle to an open stream.

### -param fcc

Four-character code specifying the stream type.

### -param plSize

Address to contain the buffer size for the optional header data.

## -remarks

The <b>AVIStreamDataSize</b> macro is defined as follows:


```cpp

#define AVIStreamDataSize(pavi, fcc, plSize) \ 
    AVIStreamReadData(pavi, fcc, NULL, plSize) 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
