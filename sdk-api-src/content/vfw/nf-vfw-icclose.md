---
UID: NF:vfw.ICClose
title: ICClose function (vfw.h)
description: The ICClose function closes a compressor or decompressor.
helpviewer_keywords: ["ICClose","ICClose function [Windows Multimedia]","_win32_ICClose","multimedia.icclose","vfw/ICClose"]
old-location: multimedia\icclose.htm
tech.root: Multimedia
ms.assetid: 9a376412-5c16-44d5-b976-0cf1f766f72a
ms.date: 12/05/2018
ms.keywords: ICClose, ICClose function [Windows Multimedia], _win32_ICClose, multimedia.icclose, vfw/ICClose
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
 - ICClose
 - vfw/ICClose
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
 - ICClose
---

# ICClose function


## -description

The <b>ICClose</b> function closes a compressor or decompressor.

## -parameters

### -param hic

Handle to a compressor or decompressor.

## -returns

Returns ICERR_OK if successful or an error otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>