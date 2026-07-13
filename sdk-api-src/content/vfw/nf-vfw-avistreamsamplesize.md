---
UID: NF:vfw.AVIStreamSampleSize
title: AVIStreamSampleSize macro (vfw.h)
description: The AVIStreamRelease macro determines the size of the buffer needed to store one sample of information from a stream. The size corresponds to the sample at the position specified by lPos.
helpviewer_keywords: ["AVIStreamSampleSize","AVIStreamSampleSize macro [Windows Multimedia]","_win32_AVIStreamSampleSize","multimedia.avistreamsamplesize","vfw/AVIStreamSampleSize"]
old-location: multimedia\avistreamsamplesize.htm
tech.root: Multimedia
ms.assetid: 24d8dae6-a9f7-4ca6-a083-1e1f59c0591c
ms.date: 07/01/2025
ms.keywords: AVIStreamSampleSize, AVIStreamSampleSize macro [Windows Multimedia], _win32_AVIStreamSampleSize, multimedia.avistreamsamplesize, vfw/AVIStreamSampleSize
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
 - AVIStreamSampleSize
 - vfw/AVIStreamSampleSize
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
 - AVIStreamSampleSize
---

# AVIStreamSampleSize macro

## -syntax

```cpp
HRESULT AVIStreamSampleSize(
     pavi,
     lPos,
     plSize
);
```

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

Returns zero if successful or an error otherwise. Possible error values include the following:<table><tr><td>AVIERR_BUFFERTOOSMALL</td><td>The buffer size was smaller than a single sample of data.</td></tr><tr><td>AVIERR_MEMORY</td><td>There was not enough memory to complete the read operation.</td></tr><tr><td>AVIERR_FILEREAD</td><td>A disk error occurred while reading the file.</td></tr></table>


## -description

The <a href="/windows/desktop/api/vfw/nf-vfw-avistreamrelease">AVIStreamRelease</a> macro determines the size of the buffer needed to store one sample of information from a stream. The size corresponds to the sample at the position specified by <i>lPos</i>.

## -parameters

### -param pavi

Handle to an open stream.

### -param lPos

Position of a sample in the stream.

### -param plSize

Address to contain the buffer size.

## -remarks

The <b>AVIStreamSampleSize</b> macro is defined as follows:


```cpp

#define AVIStreamSampleSize(pavi, lPos, plSize) \ 
    AVIStreamRead(pavi, lPos, 1, NULL, 0, plSize, NULL) 

```

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
