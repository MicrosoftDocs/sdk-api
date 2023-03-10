---
UID: NF:vfw.DrawDibGetBuffer
title: DrawDibGetBuffer function (vfw.h)
description: The DrawDibGetBuffer function retrieves the location of the buffer used by DrawDib for decompression.
helpviewer_keywords: ["DrawDibGetBuffer","DrawDibGetBuffer function [Windows Multimedia]","_win32_DrawDibGetBuffer","multimedia.drawdibgetbuffer","vfw/DrawDibGetBuffer"]
old-location: multimedia\drawdibgetbuffer.htm
tech.root: Multimedia
ms.assetid: 6b3e1d3a-2227-4a27-91aa-8767a3d76bc4
ms.date: 12/05/2018
ms.keywords: DrawDibGetBuffer, DrawDibGetBuffer function [Windows Multimedia], _win32_DrawDibGetBuffer, multimedia.drawdibgetbuffer, vfw/DrawDibGetBuffer
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
req.dll: Msvfw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawDibGetBuffer
 - vfw/DrawDibGetBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - DrawDibGetBuffer
---

# DrawDibGetBuffer function


## -description

The <b>DrawDibGetBuffer</b> function retrieves the location of the buffer used by DrawDib for decompression.

## -parameters

### -param hdd

Handle to a DrawDib DC.

### -param lpbi

Pointer to a <a href="/previous-versions//ms532284(v=vs.85)">BITMAPINFO</a> structure. This structure is made up of a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure and a 256-entry table defining the colors used by the bitmap.

### -param dwSize

Size, in bytes, of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure pointed to by <i>lpbi</i>

### -param dwFlags

Reserved; must be zero.

## -returns

Returns the address of the buffer or <b>NULL</b> if no buffer is used. if <i>lpbr</i> is not <b>NULL</b>, it is filled with a copy of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure describing the buffer.

## -see-also

<a href="/windows/desktop/Multimedia/drawdib-functions">DrawDib Functions</a>