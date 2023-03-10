---
UID: NF:vfw.AVIStreamReadFormat
title: AVIStreamReadFormat function (vfw.h)
description: The AVIStreamReadFormat function reads the stream format data.
helpviewer_keywords: ["AVIStreamReadFormat","AVIStreamReadFormat function [Windows Multimedia]","_win32_AVIStreamReadFormat","multimedia.avistreamreadformat","vfw/AVIStreamReadFormat"]
old-location: multimedia\avistreamreadformat.htm
tech.root: Multimedia
ms.assetid: 312b7d20-89b2-4102-acf6-f603610dadd6
ms.date: 12/05/2018
ms.keywords: AVIStreamReadFormat, AVIStreamReadFormat function [Windows Multimedia], _win32_AVIStreamReadFormat, multimedia.avistreamreadformat, vfw/AVIStreamReadFormat
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
 - AVIStreamReadFormat
 - vfw/AVIStreamReadFormat
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
 - AVIStreamReadFormat
---

# AVIStreamReadFormat function


## -description

The <b>AVIStreamReadFormat</b> function reads the stream format data.

## -parameters

### -param pavi

Handle to an open stream.

### -param lPos

Position in the stream used to obtain the format data.

### -param lpFormat

Pointer to a buffer to contain the format data.

### -param lpcbFormat

Pointer to a location indicating the size of the memory block referenced by <i>lpFormat</i>. On return, the value is changed to indicate the amount of data read. If <i>lpFormat</i> is <b>NULL</b>, this parameter can be used to obtain the amount of memory needed to return the format.

## -returns

Returns zero if successful or an error otherwise.

The argument <i>pavi</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -remarks

Standard video stream handlers provide format information in a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure. Standard audio stream handlers provide format information in a <a href="/previous-versions/dd743663(v=vs.85)">PCMWAVEFORMAT</a> structure. Other data streams can use other structures that describe the stream data.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>