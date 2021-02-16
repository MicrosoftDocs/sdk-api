---
UID: NF:vfw.IGetFrame.Begin
title: IGetFrame::Begin (vfw.h)
description: The Begin method prepares to extract and decompress copies of frames from a stream. Called when an application uses the AVIStreamGetFrameOpen function.
helpviewer_keywords: ["Begin","Begin method [Windows Multimedia]","Begin method [Windows Multimedia]","IGetFrame interface","IGetFrame interface [Windows Multimedia]","Begin method","IGetFrame.Begin","IGetFrame::Begin","_win32_IGetFrame_Begin","multimedia.igetframe_begin","vfw/IGetFrame::Begin"]
old-location: multimedia\igetframe_begin.htm
tech.root: Multimedia
ms.assetid: 2d2c1872-e0c3-4fea-bfb9-45b814973072
ms.date: 12/05/2018
ms.keywords: Begin, Begin method [Windows Multimedia], Begin method [Windows Multimedia],IGetFrame interface, IGetFrame interface [Windows Multimedia],Begin method, IGetFrame.Begin, IGetFrame::Begin, _win32_IGetFrame_Begin, multimedia.igetframe_begin, vfw/IGetFrame::Begin
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGetFrame::Begin
 - vfw/IGetFrame::Begin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vfw32.lib
 - Vfw32.dll
api_name:
 - IGetFrame.Begin
---

# IGetFrame::Begin


## -description

The <b>Begin</b> method prepares to extract and decompress copies of frames from a stream. Called when an application uses the <a href="/windows/desktop/api/vfw/nf-vfw-avistreamgetframeopen">AVIStreamGetFrameOpen</a> function.

## -parameters

### -param lStart

Starting frame for extracting and decompressing.

### -param lEnd

Ending frame for extracting and decompressing.

### -param lRate

Speed at which the file is read relative to its normal playback rate. Normal speed is 1000. Larger values indicate faster speeds; smaller values indicate slower speeds.


#### - ps

Pointer to the interface to a stream.

## -returns

Returns the HRESULT defined by OLE.

## -remarks

For handlers written in C++, <b>Begin</b> has the following syntax:


```cpp

HRESULT Begin(LONG lStart, LONG lEnd, LONG lRate); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>