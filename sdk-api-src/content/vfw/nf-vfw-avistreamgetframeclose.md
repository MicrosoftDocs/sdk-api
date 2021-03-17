---
UID: NF:vfw.AVIStreamGetFrameClose
title: AVIStreamGetFrameClose function (vfw.h)
description: The AVIStreamGetFrameClose function releases resources used to decompress video frames.
helpviewer_keywords: ["AVIStreamGetFrameClose","AVIStreamGetFrameClose function [Windows Multimedia]","_win32_AVIStreamGetFrameClose","multimedia.avistreamgetframeclose","vfw/AVIStreamGetFrameClose"]
old-location: multimedia\avistreamgetframeclose.htm
tech.root: Multimedia
ms.assetid: cd1fa615-ab09-4d58-9d6d-a1843c0f1d7a
ms.date: 12/05/2018
ms.keywords: AVIStreamGetFrameClose, AVIStreamGetFrameClose function [Windows Multimedia], _win32_AVIStreamGetFrameClose, multimedia.avistreamgetframeclose, vfw/AVIStreamGetFrameClose
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
 - AVIStreamGetFrameClose
 - vfw/AVIStreamGetFrameClose
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
 - AVIStreamGetFrameClose
---

# AVIStreamGetFrameClose function


## -description

The <b>AVIStreamGetFrameClose</b> function releases resources used to decompress video frames.

## -parameters

### -param pg

Handle returned from the <a href="/windows/desktop/api/vfw/nf-vfw-avistreamgetframeopen">AVIStreamGetFrameOpen</a> function. After calling this function, the handle is invalid.

## -returns

Returns zero if successful or an error otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions">AVIFile Functions</a>



<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>