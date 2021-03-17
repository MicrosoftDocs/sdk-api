---
UID: NF:vfw.ICGetInfo
title: ICGetInfo function (vfw.h)
description: The ICGetInfo function obtains information about a compressor.
helpviewer_keywords: ["ICGetInfo","ICGetInfo function [Windows Multimedia]","_win32_ICGetInfo","multimedia.icgetinfo","vfw/ICGetInfo"]
old-location: multimedia\icgetinfo.htm
tech.root: Multimedia
ms.assetid: 763dc5ef-7578-44c8-ab14-0e49644213ef
ms.date: 12/05/2018
ms.keywords: ICGetInfo, ICGetInfo function [Windows Multimedia], _win32_ICGetInfo, multimedia.icgetinfo, vfw/ICGetInfo
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
 - ICGetInfo
 - vfw/ICGetInfo
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
 - ICGetInfo
---

# ICGetInfo function


## -description

The <b>ICGetInfo</b> function obtains information about a compressor.

## -parameters

### -param hic

Handle to a compressor.

### -param picinfo

Pointer to the <a href="/windows/desktop/api/vfw/ns-vfw-icinfo">ICINFO</a> structure to return information about the compressor.

### -param cb

Size, in bytes, of the structure pointed to by <i>lpicinfo</i>.

## -returns

Returns the number of bytes copied into the structure or zero if an error occurs.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>