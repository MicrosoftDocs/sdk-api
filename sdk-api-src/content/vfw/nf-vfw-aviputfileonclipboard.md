---
UID: NF:vfw.AVIPutFileOnClipboard
title: AVIPutFileOnClipboard function (vfw.h)
description: The AVIPutFileOnClipboard function copies an AVI file to the clipboard.
helpviewer_keywords: ["AVIPutFileOnClipboard","AVIPutFileOnClipboard function [Windows Multimedia]","_win32_AVIPutFileOnClipboard","multimedia.aviputfileonclipboard","vfw/AVIPutFileOnClipboard"]
old-location: multimedia\aviputfileonclipboard.htm
tech.root: Multimedia
ms.assetid: 5b2bf73d-9a09-4eec-bbb2-893fe584e3e0
ms.date: 12/05/2018
ms.keywords: AVIPutFileOnClipboard, AVIPutFileOnClipboard function [Windows Multimedia], _win32_AVIPutFileOnClipboard, multimedia.aviputfileonclipboard, vfw/AVIPutFileOnClipboard
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
 - AVIPutFileOnClipboard
 - vfw/AVIPutFileOnClipboard
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
 - AVIPutFileOnClipboard
---

# AVIPutFileOnClipboard function


## -description

The <b>AVIPutFileOnClipboard</b> function copies an AVI file to the clipboard.

## -parameters

### -param pf

Handle to an open AVI file.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

This function also copies data with the CF_DIB, CF_PALETTE, and CF_WAVE clipboard flags onto the clipboard using the first frame of the first video stream of the file as a DIB and using the audio stream as CF_WAVE.

The argument pf is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavifile">IAVIFile</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>