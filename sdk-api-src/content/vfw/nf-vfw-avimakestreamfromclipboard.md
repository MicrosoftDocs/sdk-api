---
UID: NF:vfw.AVIMakeStreamFromClipboard
title: AVIMakeStreamFromClipboard function (vfw.h)
description: The AVIMakeStreamFromClipboard function creates an editable stream from stream data on the clipboard.
helpviewer_keywords: ["AVIMakeStreamFromClipboard","AVIMakeStreamFromClipboard function [Windows Multimedia]","_win32_AVIMakeStreamFromClipboard","multimedia.avimakestreamfromclipboard","vfw/AVIMakeStreamFromClipboard"]
old-location: multimedia\avimakestreamfromclipboard.htm
tech.root: Multimedia
ms.assetid: e41f4ef2-bb57-4a92-b382-7faa106d2aa0
ms.date: 12/05/2018
ms.keywords: AVIMakeStreamFromClipboard, AVIMakeStreamFromClipboard function [Windows Multimedia], _win32_AVIMakeStreamFromClipboard, multimedia.avimakestreamfromclipboard, vfw/AVIMakeStreamFromClipboard
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
 - AVIMakeStreamFromClipboard
 - vfw/AVIMakeStreamFromClipboard
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
 - AVIMakeStreamFromClipboard
---

# AVIMakeStreamFromClipboard function


## -description

The <b>AVIMakeStreamFromClipboard</b> function creates an editable stream from stream data on the clipboard.

## -parameters

### -param cfFormat

Clipboard flag.

### -param hGlobal

Handle to stream data on the clipboard.

### -param ppstream

Handle to the created stream.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

When an application finishes using the editable stream, it must release the stream to free the resources associated with it.

The argument ppstream is the address of a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>