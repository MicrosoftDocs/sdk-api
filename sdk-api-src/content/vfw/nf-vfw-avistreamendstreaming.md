---
UID: NF:vfw.AVIStreamEndStreaming
title: AVIStreamEndStreaming function (vfw.h)
description: The AVIStreamEndStreaming function ends streaming.
helpviewer_keywords: ["AVIStreamEndStreaming","AVIStreamEndStreaming function [Windows Multimedia]","_win32_AVIStreamEndStreaming","multimedia.avistreamendstreaming","vfw/AVIStreamEndStreaming"]
old-location: multimedia\avistreamendstreaming.htm
tech.root: Multimedia
ms.assetid: 8555bc24-c017-4d02-854b-e64cf9e8ae1b
ms.date: 12/05/2018
ms.keywords: AVIStreamEndStreaming, AVIStreamEndStreaming function [Windows Multimedia], _win32_AVIStreamEndStreaming, multimedia.avistreamendstreaming, vfw/AVIStreamEndStreaming
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
 - AVIStreamEndStreaming
 - vfw/AVIStreamEndStreaming
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
 - AVIStreamEndStreaming
---

# AVIStreamEndStreaming function


## -description

The <b>AVIStreamEndStreaming</b> function ends streaming.

## -parameters

### -param pavi

Pointer to a stream.

## -returns

Returns zero if successful or an error otherwise.

## -remarks

Many stream implementations ignore this function.

The argument <i>pavi</i> contains a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>