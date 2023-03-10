---
UID: NF:vfw.AVIStreamGetFrameOpen
title: AVIStreamGetFrameOpen function (vfw.h)
description: The AVIStreamGetFrameOpen function prepares to decompress video frames from the specified video stream.
helpviewer_keywords: ["AVIStreamGetFrameOpen","AVIStreamGetFrameOpen function [Windows Multimedia]","_win32_AVIStreamGetFrameOpen","multimedia.avistreamgetframeopen","vfw/AVIStreamGetFrameOpen"]
old-location: multimedia\avistreamgetframeopen.htm
tech.root: Multimedia
ms.assetid: 467560b2-f79f-49ab-b019-d6315f0c2030
ms.date: 12/05/2018
ms.keywords: AVIStreamGetFrameOpen, AVIStreamGetFrameOpen function [Windows Multimedia], _win32_AVIStreamGetFrameOpen, multimedia.avistreamgetframeopen, vfw/AVIStreamGetFrameOpen
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
 - AVIStreamGetFrameOpen
 - vfw/AVIStreamGetFrameOpen
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
 - AVIStreamGetFrameOpen
---

# AVIStreamGetFrameOpen function


## -description

The <b>AVIStreamGetFrameOpen</b> function prepares to decompress video frames from the specified video stream.

## -parameters

### -param pavi

Pointer to the video stream used as the video source.

### -param lpbiWanted

Pointer to a structure that defines the desired video format. Specify <b>NULL</b> to use a default format. You can also specify AVIGETFRAMEF_BESTDISPLAYFMT to decode the frames to the best format for your display.

## -returns

Returns a <b>GetFrame</b> object that can be used with the <a href="/windows/desktop/api/vfw/nf-vfw-avistreamgetframe">AVIStreamGetFrame</a> function. If the system cannot find a decompressor that can decompress the stream to the given format, or to any RGB format, the function returns <b>NULL</b>.

The argument <i>pavi</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>