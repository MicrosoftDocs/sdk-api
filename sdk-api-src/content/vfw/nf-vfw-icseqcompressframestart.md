---
UID: NF:vfw.ICSeqCompressFrameStart
title: ICSeqCompressFrameStart function (vfw.h)
description: The ICSeqCompressFrameStart function initializes resources for compressing a sequence of frames using the ICSeqCompressFrame function.
helpviewer_keywords: ["ICSeqCompressFrameStart","ICSeqCompressFrameStart function [Windows Multimedia]","_win32_ICSeqCompressFrameStart","multimedia.icseqcompressframestart","vfw/ICSeqCompressFrameStart"]
old-location: multimedia\icseqcompressframestart.htm
tech.root: Multimedia
ms.assetid: 90103468-fcdc-4c40-b328-29fe467b9039
ms.date: 12/05/2018
ms.keywords: ICSeqCompressFrameStart, ICSeqCompressFrameStart function [Windows Multimedia], _win32_ICSeqCompressFrameStart, multimedia.icseqcompressframestart, vfw/ICSeqCompressFrameStart
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
 - ICSeqCompressFrameStart
 - vfw/ICSeqCompressFrameStart
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
 - ICSeqCompressFrameStart
---

# ICSeqCompressFrameStart function


## -description

The <b>ICSeqCompressFrameStart</b> function initializes resources for compressing a sequence of frames using the <a href="/windows/desktop/api/vfw/nf-vfw-icseqcompressframe">ICSeqCompressFrame</a> function.

## -parameters

### -param pc

Pointer to a <a href="/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a> structure initialized with information for compression.

### -param lpbiIn

Format of the data to be compressed.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.

## -remarks

This function uses a <a href="/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a> structure to provide settings for the specified compressor and intersperses key frames at the rate specified by the <b>lKey</b> member of <b>COMPVARS</b>. You can specify values for the data rate for the sequence and the key-frame frequency by using the appropriate members of <b>COMPVARS</b>.

Use the <b>ICSeqCompressFrameStart</b>, <a href="/windows/desktop/api/vfw/nf-vfw-icseqcompressframe">ICSeqCompressFrame</a>, and <a href="/windows/desktop/api/vfw/nf-vfw-icseqcompressframeend">ICSeqCompressFrameEnd</a> functions to compress a sequence of frames to a specified data rate and number of key frames.

When finished with compression, use the <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorfree">ICCompressorFree</a> function to release the resources specified in <a href="/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a>.


<a href="/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a> needs to be initialized before you use this function. You can initialize the structure manually or you can allow the user to specify a compressor and initialize a <b>COMPVARS</b> structure by using the <a href="/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a> function.

## -see-also

<a href="/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>