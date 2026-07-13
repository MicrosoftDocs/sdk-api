---
UID: NF:vfw.AVIStreamInfoA
title: AVIStreamInfoA function (vfw.h)
description: The AVIStreamInfo function obtains stream header information. (ANSI)
helpviewer_keywords: ["AVIStreamInfoA", "vfw/AVIStreamInfoA"]
old-location: multimedia\avistreaminfo.htm
tech.root: Multimedia
ms.assetid: 7a1ba29b-e8ba-435d-a551-c9184631971c
ms.date: 12/05/2018
ms.keywords: AVIStreamInfo, AVIStreamInfo function [Windows Multimedia], AVIStreamInfoA, AVIStreamInfoW, _win32_AVIStreamInfo, multimedia.avistreaminfo, vfw/AVIStreamInfo, vfw/AVIStreamInfoA, vfw/AVIStreamInfoW
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AVIStreamInfoW (Unicode) and AVIStreamInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVIStreamInfoA
 - vfw/AVIStreamInfoA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
 - Ext-MS-Win-Media-Avi-L1-1-0.dll
api_name:
 - AVIStreamInfo
 - AVIStreamInfoA
 - AVIStreamInfoW
---

# AVIStreamInfoA function


## -description

The <b>AVIStreamInfo</b> function obtains stream header information.

## -parameters

### -param pavi

Handle to an open stream.

### -param psi

Pointer to a structure to contain the stream information.

### -param lSize

Size, in bytes, of the structure used for psi.

## -returns

Returns zero if successful or an error otherwise.

The argument <i>pavi</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>

## -remarks

> [!NOTE]
> The vfw.h header defines AVISTREAMINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
