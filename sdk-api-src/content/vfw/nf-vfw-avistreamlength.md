---
UID: NF:vfw.AVIStreamLength
title: AVIStreamLength function (vfw.h)
description: The AVIStreamLength function returns the length of the stream.
helpviewer_keywords: ["AVIStreamLength","AVIStreamLength function [Windows Multimedia]","_win32_AVIStreamLength","multimedia.avistreamlength","vfw/AVIStreamLength"]
old-location: multimedia\avistreamlength.htm
tech.root: Multimedia
ms.assetid: 5fc5dd31-9f2d-48c8-8d7e-76add4608473
ms.date: 12/05/2018
ms.keywords: AVIStreamLength, AVIStreamLength function [Windows Multimedia], _win32_AVIStreamLength, multimedia.avistreamlength, vfw/AVIStreamLength
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
 - AVIStreamLength
 - vfw/AVIStreamLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-media-avi-l1-1-0.dll
 - Avifil32.dll
api_name:
 - AVIStreamLength
---

# AVIStreamLength function


## -description

The <b>AVIStreamLength</b> function returns the length of the stream.

## -parameters

### -param pavi

Handle to an open stream.

## -returns

Returns the stream's length, in samples, if successful or -1 otherwise.

The argument <i>pavi</i> is a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>