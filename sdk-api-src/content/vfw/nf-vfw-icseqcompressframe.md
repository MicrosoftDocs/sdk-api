---
UID: NF:vfw.ICSeqCompressFrame
title: ICSeqCompressFrame function
author: windows-sdk-content
description: The ICSeqCompressFrame function compresses one frame in a sequence of frames.
old-location: multimedia\icseqcompressframe.htm
tech.root: Multimedia
ms.assetid: 6159e455-1e1a-4aa5-9d75-53cd2af2656a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICSeqCompressFrame, ICSeqCompressFrame function [Windows Multimedia], _win32_ICSeqCompressFrame, multimedia.icseqcompressframe, vfw/ICSeqCompressFrame
ms.topic: function
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
---

# ICSeqCompressFrame function


## -description



The <b>ICSeqCompressFrame</b> function compresses one frame in a sequence of frames.




## -parameters




### -param pc

Pointer to a <a href="https://msdn.microsoft.com/b34378cb-ccf0-4d97-a952-1966999e3f65">COMPVARS</a> structure initialized with information about the compression.


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



This function uses a <a href="https://msdn.microsoft.com/b34378cb-ccf0-4d97-a952-1966999e3f65">COMPVARS</a> structure to provide settings for the specified compressor and intersperses key frames at the rate specified by the <a href="https://msdn.microsoft.com/90103468-fcdc-4c40-b328-29fe467b9039">ICSeqCompressorFrameStart</a> function. You can specify values for the data rate for the sequence and the key-frame frequency by using the appropriate members of <b>COMPVARS</b>.

Use this function instead of the <a href="https://msdn.microsoft.com/99e7d87a-cbf5-42d3-897c-5f5c8860a13a">ICCompress</a> function to compress a video sequence.

You can allow the user to specify a compressor and initialize a <a href="https://msdn.microsoft.com/b34378cb-ccf0-4d97-a952-1966999e3f65">COMPVARS</a> structure by using the <a href="https://msdn.microsoft.com/4a58df6a-9ac4-44bb-8c49-338bb60193fc">ICCompressorChoose</a> function. Or, you can initialize a <b>COMPVARS</b> structure manually.

Use the <a href="https://msdn.microsoft.com/90103468-fcdc-4c40-b328-29fe467b9039">ICSeqCompressFrameStart</a>, <b>ICSeqCompressFrame</b>, and <a href="https://msdn.microsoft.com/3fdcd18d-4ee7-4b5a-871d-61316c716e06">ICSeqCompressFrameEnd</a> functions to compress a sequence of frames to a specified data rate and number of key frames. Use <b>ICSeqCompressFrame</b> once for each frame to be compressed.

When finished with compression, use the <a href="https://msdn.microsoft.com/6d0c9a7d-6458-4330-af74-3f471555cbfc">ICCompressorFree</a> function to release the resources specified by <a href="https://msdn.microsoft.com/b34378cb-ccf0-4d97-a952-1966999e3f65">COMPVARS</a>.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

