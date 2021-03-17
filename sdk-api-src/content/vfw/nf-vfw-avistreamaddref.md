---
UID: NF:vfw.AVIStreamAddRef
title: AVIStreamAddRef function (vfw.h)
description: The AVIStreamAddRef function increments the reference count of an AVI stream.
helpviewer_keywords: ["AVIStreamAddRef","AVIStreamAddRef function [Windows Multimedia]","_win32_AVIStreamAddRef","multimedia.avistreamaddref","vfw/AVIStreamAddRef"]
old-location: multimedia\avistreamaddref.htm
tech.root: Multimedia
ms.assetid: 4d5e6b0f-6753-4ac0-b074-51016634cc10
ms.date: 12/05/2018
ms.keywords: AVIStreamAddRef, AVIStreamAddRef function [Windows Multimedia], _win32_AVIStreamAddRef, multimedia.avistreamaddref, vfw/AVIStreamAddRef
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
 - AVIStreamAddRef
 - vfw/AVIStreamAddRef
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
 - AVIStreamAddRef
---

# AVIStreamAddRef function


## -description

The <b>AVIStreamAddRef</b> function increments the reference count of an AVI stream.

## -parameters

### -param pavi

Handle to an open AVI stream.

## -returns

Returns the current reference count of the stream. This value should be used only for debugging purposes.

## -remarks

The argument <i>pavi</i> contains a pointer to an <a href="/windows/desktop/api/vfw/nn-vfw-iavistream">IAVIStream</a> interface.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>