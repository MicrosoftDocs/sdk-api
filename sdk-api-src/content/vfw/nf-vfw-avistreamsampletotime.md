---
UID: NF:vfw.AVIStreamSampleToTime
title: AVIStreamSampleToTime function (vfw.h)
description: The AVIStreamSampleToTime function converts a stream position from samples to milliseconds.
helpviewer_keywords: ["AVIStreamSampleToTime","AVIStreamSampleToTime function [Windows Multimedia]","_win32_AVIStreamSampleToTime","multimedia.avistreamsampletotime","vfw/AVIStreamSampleToTime"]
old-location: multimedia\avistreamsampletotime.htm
tech.root: Multimedia
ms.assetid: 376819cb-f803-4610-a9e8-29dc7059f203
ms.date: 12/05/2018
ms.keywords: AVIStreamSampleToTime, AVIStreamSampleToTime function [Windows Multimedia], _win32_AVIStreamSampleToTime, multimedia.avistreamsampletotime, vfw/AVIStreamSampleToTime
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
 - AVIStreamSampleToTime
 - vfw/AVIStreamSampleToTime
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
 - AVIStreamSampleToTime
---

# AVIStreamSampleToTime function


## -description

The <b>AVIStreamSampleToTime</b> function converts a stream position from samples to milliseconds.

## -parameters

### -param pavi

Handle to an open stream.

### -param lSample

Position information. A sample can correspond to blocks of audio, a video frame, or other format, depending on the stream type.

## -returns

Returns the converted time if successful or −1 otherwise.

## -remarks

The argument <i>pavi</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>