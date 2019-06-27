---
UID: NF:vfw.ICSeqCompressFrame
title: ICSeqCompressFrame function (vfw.h)
author: windows-sdk-content
description: The ICSeqCompressFrame function compresses one frame in a sequence of frames.
old-location: multimedia\icseqcompressframe.htm
tech.root: Multimedia
ms.assetid: 6159e455-1e1a-4aa5-9d75-53cd2af2656a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICSeqCompressFrame, ICSeqCompressFrame function [Windows Multimedia], _win32_ICSeqCompressFrame, multimedia.icseqcompressframe, vfw/ICSeqCompressFrame
ms.topic: function
f1_keywords: 
 - "vfw/ICSeqCompressFrame"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - ICSeqCompressFrame
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICSeqCompressFrame function


## -description



The <b>ICSeqCompressFrame</b> function compresses one frame in a sequence of frames.




## -parameters




### -param pc

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a> structure initialized with information about the compression.


### -param uiFlags

Reserved; must be zero.


### -param lpBits

Pointer to the data bits to compress. (The data bits exclude header or format information.)


### -param pfKey

Returns whether or not the frame was compressed into a key frame.


### -param plSize

Maximum size desired for the compressed image. The compressor might not be able to compress the data to fit within this size. When the function returns, the parameter points to the size of the compressed image. Images sizes are specified in bytes.


## -returns



Returns the address of the compressed bits if successful or <b>NULL</b> otherwise.




## -remarks



This function uses a <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a> structure to provide settings for the specified compressor and intersperses key frames at the rate specified by the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icseqcompressframestart">ICSeqCompressorFrameStart</a> function. You can specify values for the data rate for the sequence and the key-frame frequency by using the appropriate members of <b>COMPVARS</b>.

Use this function instead of the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iccompress">ICCompress</a> function to compress a video sequence.

You can allow the user to specify a compressor and initialize a <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a> structure by using the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iccompressorchoose">ICCompressorChoose</a> function. Or, you can initialize a <b>COMPVARS</b> structure manually.

Use the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icseqcompressframestart">ICSeqCompressFrameStart</a>, <b>ICSeqCompressFrame</b>, and <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icseqcompressframeend">ICSeqCompressFrameEnd</a> functions to compress a sequence of frames to a specified data rate and number of key frames. Use <b>ICSeqCompressFrame</b> once for each frame to be compressed.

When finished with compression, use the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-iccompressorfree">ICCompressorFree</a> function to release the resources specified by <a href="https://docs.microsoft.com/windows/desktop/api/vfw/ns-vfw-compvars">COMPVARS</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-functions">Video Compression Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

