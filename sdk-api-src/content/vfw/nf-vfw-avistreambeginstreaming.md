---
UID: NF:vfw.AVIStreamBeginStreaming
title: AVIStreamBeginStreaming function (vfw.h)
description: The AVIStreamBeginStreaming function specifies the parameters used in streaming and lets a stream handler prepare for streaming.
helpviewer_keywords: ["AVIStreamBeginStreaming","AVIStreamBeginStreaming function [Windows Multimedia]","_win32_AVIStreamBeginStreaming","multimedia.avistreambeginstreaming","vfw/AVIStreamBeginStreaming"]
old-location: multimedia\avistreambeginstreaming.htm
tech.root: Multimedia
ms.assetid: 79bf7c19-56b6-48fa-a673-32ce1bcdddad
ms.date: 12/05/2018
ms.keywords: AVIStreamBeginStreaming, AVIStreamBeginStreaming function [Windows Multimedia], _win32_AVIStreamBeginStreaming, multimedia.avistreambeginstreaming, vfw/AVIStreamBeginStreaming
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
 - AVIStreamBeginStreaming
 - vfw/AVIStreamBeginStreaming
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
 - AVIStreamBeginStreaming
---

# AVIStreamBeginStreaming function


## -description

The <b>AVIStreamBeginStreaming</b> function specifies the parameters used in streaming and lets a stream handler prepare for streaming.

## -parameters

### -param pavi

Pointer to a stream.

### -param lStart

Starting frame for streaming.

### -param lEnd

Ending frame for streaming.

### -param lRate

Speed at which the file is read relative to its natural speed. Specify 1000 for the normal speed. Values less than 1000 indicate a slower-than-normal speed; values greater than 1000 indicate a faster-than-normal speed.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

The argument <i>pavi</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>