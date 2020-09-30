---
UID: NF:vfw.ICInfo
title: ICInfo function (vfw.h)
description: The ICInfo function retrieves information about specific installed compressors or enumerates the installed compressors.
helpviewer_keywords: ["ICInfo","ICInfo function [Windows Multimedia]","_win32_ICInfo","multimedia.icinfo","vfw/ICInfo"]
old-location: multimedia\icinfo.htm
tech.root: Multimedia
ms.assetid: 755ff010-3edc-4e13-9c8f-104a6d1f590a
ms.date: 12/05/2018
ms.keywords: ICInfo, ICInfo function [Windows Multimedia], _win32_ICInfo, multimedia.icinfo, vfw/ICInfo
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
 - ICInfo
 - vfw/ICInfo
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
 - ICInfo
---

# ICInfo function


## -description

The <b>ICInfo</b> function retrieves information about specific installed compressors or enumerates the installed compressors.

## -parameters

### -param fccType

Four-character code indicating the type of compressor. Specify zero to match all compressor types.

### -param fccHandler

Four-character code identifying a specific compressor or a number between zero and the number of installed compressors of the type specified by <i>fccType</i>.

### -param lpicinfo

Pointer to a <a href="/windows/desktop/api/vfw/ns-vfw-icinfo">ICINFO</a> structure to return information about the compressor.

## -returns

Returns <b>TRUE</b> if successful or an error otherwise.

## -remarks

To enumerate the compressors or decompressors, specify an integer for <i>fccHandler</i>. This function returns information for integers between zero and the number of installed compressors or decompressors of the type specified for <i>fccType</i>.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>