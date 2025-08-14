---
UID: NF:vfw.AVIStreamSetFormat
title: AVIStreamSetFormat function (vfw.h)
description: The AVIStreamSetFormat function sets the format of a stream at the specified position.
helpviewer_keywords: ["AVIStreamSetFormat","AVIStreamSetFormat function [Windows Multimedia]","_win32_AVIStreamSetFormat","multimedia.avistreamsetformat","vfw/AVIStreamSetFormat"]
old-location: multimedia\avistreamsetformat.htm
tech.root: Multimedia
ms.assetid: b896f674-823d-49c9-8e48-c5081e37a13a
ms.date: 12/05/2018
ms.keywords: AVIStreamSetFormat, AVIStreamSetFormat function [Windows Multimedia], _win32_AVIStreamSetFormat, multimedia.avistreamsetformat, vfw/AVIStreamSetFormat
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
req.lib: Vfw32.lib
req.dll: Avifil32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVIStreamSetFormat
 - vfw/AVIStreamSetFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-media-avi-l1-1-0.dll
 - Avifil32.dll
api_name:
 - AVIStreamSetFormat
---

# AVIStreamSetFormat function


## -description

The <b>AVIStreamSetFormat</b> function sets the format of a stream at the specified position.

## -parameters

### -param pavi

Handle to an open stream.

### -param lPos

Position in the stream to receive the format.

### -param lpFormat

Pointer to a structure containing the new format.

### -param cbFormat

Size, in bytes, of the block of memory referenced by <i>lpFormat</i>.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

The handler for writing AVI files does not accept format changes. Besides setting the initial format for a stream, only changes in the palette of a video stream are allowed in an AVI file. The palette change must occur after any frames already written to the AVI file. Other handlers might impose different restrictions.

The argument <i>pavi</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>