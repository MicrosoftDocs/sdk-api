---
UID: NF:vfw.ICRemove
title: ICRemove function (vfw.h)
description: The ICRemove function removes an installed compressor.
helpviewer_keywords: ["ICRemove","ICRemove function [Windows Multimedia]","_win32_ICRemove","multimedia.icremove","vfw/ICRemove"]
old-location: multimedia\icremove.htm
tech.root: Multimedia
ms.assetid: c5f2638a-6b75-4e30-8420-94011c73f5bd
ms.date: 12/05/2018
ms.keywords: ICRemove, ICRemove function [Windows Multimedia], _win32_ICRemove, multimedia.icremove, vfw/ICRemove
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
 - ICRemove
 - vfw/ICRemove
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
 - ICRemove
---

# ICRemove function


## -description

The <b>ICRemove</b> function removes an installed compressor.

## -parameters

### -param fccType

Four-character code indicating the type of data used by the compressor or decompressor. Specify "VIDC" for a video compressor or decompressor.

### -param fccHandler

Four-character code identifying a specific compressor or a number between zero and the number of installed compressors of the type specified by <i>fccType</i>.

### -param wFlags

Reserved; do not use.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>