---
UID: NF:vfw.AVIStreamReadData
title: AVIStreamReadData function (vfw.h)
description: The AVIStreamReadData function reads optional header data from a stream.
helpviewer_keywords: ["AVIStreamReadData","AVIStreamReadData function [Windows Multimedia]","_win32_AVIStreamReadData","multimedia.avistreamreaddata","vfw/AVIStreamReadData"]
old-location: multimedia\avistreamreaddata.htm
tech.root: Multimedia
ms.assetid: 87a787e8-547a-4c35-ba65-a592bd037063
ms.date: 12/05/2018
ms.keywords: AVIStreamReadData, AVIStreamReadData function [Windows Multimedia], _win32_AVIStreamReadData, multimedia.avistreamreaddata, vfw/AVIStreamReadData
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
 - AVIStreamReadData
 - vfw/AVIStreamReadData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Avifil32.dll
api_name:
 - AVIStreamReadData
---

# AVIStreamReadData function


## -description

The <b>AVIStreamReadData</b> function reads optional header data from a stream.

## -parameters

### -param pavi

Handle to an open stream.

### -param fcc

Four-character code identifying the data.

### -param lp

Pointer to the buffer to contain the optional header data.

### -param lpcb

Pointer to the location that specifies the buffer size used for <i>lpData</i>. If the read is successful, AVIFile changes this value to indicate the amount of data written into the buffer for <i>lpData</i>.

## -returns

Returns zero if successful or an error otherwise. The return value AVIERR_NODATA indicates the system could not find any data with the specified chunk identifier.

## -remarks

This function retrieves only optional header information from the stream. This information is custom and does not have a set format.

The argument <i>pavi</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>