---
UID: NF:vfw.IGetFrame.SetFormat
title: IGetFrame::SetFormat (vfw.h)
description: The SetFormat method sets the decompressed image format of the frames being extracted and optionally provides a buffer for the decompression operation.
helpviewer_keywords: ["IGetFrame interface [Windows Multimedia]","SetFormat method","IGetFrame.SetFormat","IGetFrame::SetFormat","SetFormat","SetFormat method [Windows Multimedia]","SetFormat method [Windows Multimedia]","IGetFrame interface","_win32_IGetFrame_SetFormat","multimedia.igetframe_setformat","vfw/IGetFrame::SetFormat"]
old-location: multimedia\igetframe_setformat.htm
tech.root: Multimedia
ms.assetid: 96a2afa5-af90-47e0-949a-a1498ed7f82e
ms.date: 12/05/2018
ms.keywords: IGetFrame interface [Windows Multimedia],SetFormat method, IGetFrame.SetFormat, IGetFrame::SetFormat, SetFormat, SetFormat method [Windows Multimedia], SetFormat method [Windows Multimedia],IGetFrame interface, _win32_IGetFrame_SetFormat, multimedia.igetframe_setformat, vfw/IGetFrame::SetFormat
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
 - IGetFrame::SetFormat
 - vfw/IGetFrame::SetFormat
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
 - IGetFrame.SetFormat
---

# IGetFrame::SetFormat


## -description

The <b>SetFormat</b> method sets the decompressed image format of the frames being extracted and optionally provides a buffer for the decompression operation.

## -parameters

### -param lpbi

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure defining the decompressed image format. You can also specify <b>NULL</b> or the value <code>((LPBITMAPINFOHEADER) 1)</code> for this parameter. <b>NULL</b> causes the decompressor to choose a format that is appropriate for editing (normally a 24-bit image depth format). The value <code>((LPBITMAPINFOHEADER) 1)</code> causes the decompressor to choose a format appropriate for the current display mode.

### -param lpBits

Pointer to a buffer to contain the decompressed image data. Specify <b>NULL</b> to have this method allocate a buffer.

### -param x

The x-coordinate of the destination rectangle within the DIB specified by <i>lpbi</i>. This parameter is used when <i>lpBits</i> is not <b>NULL</b>.

### -param y

The y-coordinate of the destination rectangle within the DIB specified by <i>lpbi</i>. This parameter is used when <i>lpBits</i> is not <b>NULL</b>.

### -param dx

Width of the destination rectangle. This parameter is used when <i>lpBits</i> is not <b>NULL</b>.

### -param dy

Height of the destination rectangle. This parameter is used when <i>lpBits</i> is not <b>NULL</b>.


#### - ps

Pointer to the interface to a stream.

## -returns

Returns <b>NOERROR</b> if successful, <b>E_OUTOFMEMORY</b> if the decompressed image is larger than the buffer size, or <b>E_FAIL</b> otherwise.

## -remarks

The <i>x</i>, <i>y</i>, <i>dx</i>, and <i>dy</i> parameters identify the portion of the bitmap specified by <i>lpbi</i> and <i>lpBits</i> that receives the decompressed image.

For handlers written in C++, <b>SetFormat</b> has the following syntax:


```cpp

HRESULT SetFormat(LPBITMAPINFOHEADER lpbi, LPVOID lpBits, int x, 
    int y, int dx, int dy); 
 

```

## -see-also

<a href="/windows/desktop/Multimedia/custom-file-and-stream-handler-interfaces">Custom File and Stream Handler Interfaces</a>



<a href="/windows/desktop/Multimedia/custom-file-and-stream-handlers">Custom File and Stream Handlers</a>