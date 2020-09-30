---
UID: NF:vfw.AVIStreamTimeToSample
title: AVIStreamTimeToSample function (vfw.h)
description: The AVIStreamTimeToSample function converts from milliseconds to samples.
helpviewer_keywords: ["AVIStreamTimeToSample","AVIStreamTimeToSample function [Windows Multimedia]","_win32_AVIStreamTimeToSample","multimedia.avistreamtimetosample","vfw/AVIStreamTimeToSample"]
old-location: multimedia\avistreamtimetosample.htm
tech.root: Multimedia
ms.assetid: 2be5ad91-2371-4564-a679-c593f497a785
ms.date: 12/05/2018
ms.keywords: AVIStreamTimeToSample, AVIStreamTimeToSample function [Windows Multimedia], _win32_AVIStreamTimeToSample, multimedia.avistreamtimetosample, vfw/AVIStreamTimeToSample
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
 - AVIStreamTimeToSample
 - vfw/AVIStreamTimeToSample
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
 - AVIStreamTimeToSample
---

# AVIStreamTimeToSample function


## -description

The <b>AVIStreamTimeToSample</b> function converts from milliseconds to samples.

## -parameters

### -param pavi

Handle to an open stream.

### -param lTime

Time, expressed in milliseconds.

## -returns

Returns the converted time if successful or -1 otherwise.

## -remarks

Samples typically correspond to audio samples or video frames. Other stream types might support different formats than these.

The argument <i>pavi</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>