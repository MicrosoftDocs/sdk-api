---
UID: NF:vfw.ICSeqCompressFrameEnd
title: ICSeqCompressFrameEnd function (vfw.h)
description: The ICSeqCompressFrameEnd function ends sequence compression that was initiated by using the ICSeqCompressFrameStart and ICSeqCompressFrame functions.
helpviewer_keywords: ["ICSeqCompressFrameEnd","ICSeqCompressFrameEnd function [Windows Multimedia]","_win32_ICSeqCompressFrameEnd","multimedia.icseqcompressframeend","vfw/ICSeqCompressFrameEnd"]
old-location: multimedia\icseqcompressframeend.htm
tech.root: Multimedia
ms.assetid: 3fdcd18d-4ee7-4b5a-871d-61316c716e06
ms.date: 12/05/2018
ms.keywords: ICSeqCompressFrameEnd, ICSeqCompressFrameEnd function [Windows Multimedia], _win32_ICSeqCompressFrameEnd, multimedia.icseqcompressframeend, vfw/ICSeqCompressFrameEnd
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
 - ICSeqCompressFrameEnd
 - vfw/ICSeqCompressFrameEnd
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
 - ICSeqCompressFrameEnd
---

# ICSeqCompressFrameEnd function


## -description

The <b>ICSeqCompressFrameEnd</b> function ends sequence compression that was initiated by using the <a href="/windows/desktop/api/vfw/nf-vfw-icseqcompressframestart">ICSeqCompressFrameStart</a> and <a href="/windows/desktop/api/vfw/nf-vfw-icseqcompressframe">ICSeqCompressFrame</a> functions.

## -parameters

### -param pc

Pointer to a <a href="/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a> structure used during sequence compression.

## -returns

This function does not return a value.

## -remarks

When finished with compression, use the <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorfree">ICCompressorFree</a> function to release the resources specified by <a href="/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a>.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>