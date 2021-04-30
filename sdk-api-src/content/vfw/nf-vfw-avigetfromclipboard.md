---
UID: NF:vfw.AVIGetFromClipboard
title: AVIGetFromClipboard function (vfw.h)
description: The AVIGetFromClipboard function copies an AVI file from the clipboard.
helpviewer_keywords: ["AVIGetFromClipboard","AVIGetFromClipboard function [Windows Multimedia]","_win32_AVIGetFromClipboard","multimedia.avigetfromclipboard","vfw/AVIGetFromClipboard"]
old-location: multimedia\avigetfromclipboard.htm
tech.root: Multimedia
ms.assetid: 17115441-8809-4fc2-9749-0e9d4c4f9cac
ms.date: 12/05/2018
ms.keywords: AVIGetFromClipboard, AVIGetFromClipboard function [Windows Multimedia], _win32_AVIGetFromClipboard, multimedia.avigetfromclipboard, vfw/AVIGetFromClipboard
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
 - AVIGetFromClipboard
 - vfw/AVIGetFromClipboard
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
 - AVIGetFromClipboard
---

# AVIGetFromClipboard function


## -description

The <b>AVIGetFromClipboard</b> function copies an AVI file from the clipboard.

## -parameters

### -param lppf

Pointer to the location used to return the handle created for the AVI file.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

If the clipboard does not contain an AVI file, <b>AVIGetFromClipboard</b> also can copy data with the CF_DIB or CF_WAVE clipboard flags to an AVI file. In this case, the function creates an AVI file with one DIB stream and one waveform-audio stream, and fills each stream with the data from the clipboard.

The argument <i>lppf</i> is the address of a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavifile">IAVIFile</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>