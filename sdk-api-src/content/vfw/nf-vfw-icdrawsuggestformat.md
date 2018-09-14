---
UID: NF:vfw.ICDrawSuggestFormat
title: ICDrawSuggestFormat function
author: windows-sdk-content
description: The ICDrawSuggestFormat function notifies the drawing handler to suggest the input data format.
old-location: multimedia\icdrawsuggestformat.htm
tech.root: Multimedia
ms.assetid: 748d09a6-52db-4bd0-9006-6ee96f07a74b
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICDrawSuggestFormat, ICDrawSuggestFormat function [Windows Multimedia], _win32_ICDrawSuggestFormat, multimedia.icdrawsuggestformat, vfw/ICDrawSuggestFormat
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICDrawSuggestFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDrawSuggestFormat function


## -description



The <b>ICDrawSuggestFormat</b> function notifies the drawing handler to suggest the input data format.




## -parameters




### -param hic

Handle to the driver to use.


### -param lpbiIn

Pointer to a structure containing the format of the compressed data. For bitmaps, this is a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure.


### -param lpbiOut

Pointer to a structure to return the suggested format. The drawing handler can receive and draw data from this format. For bitmaps, this is a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure.


### -param dxSrc

Width of the source rectangle.


### -param dySrc

Height of the source rectangle.


### -param dxDst

Width of the destination rectangle.


### -param dyDst

Height of the destination rectangle.


### -param hicDecomp

Decompressor that can use the format of data in <i>lpbiIn</i>.


## -returns



Returns <b>ICERR_OK</b> if successful or an error otherwise.
          




## -remarks



Applications can use this function to determine alternative input formats that a drawing handler can decompress and if the drawing handler can stretch data. If the drawing handler cannot stretch data as requested, the application might have to stretch the data.

If the drawing handler cannot decompress a format provided by an application, use the <a href="https://msdn.microsoft.com/779b63db-6b1d-4eb5-9df5-bb847b35863d">ICDecompress</a>, <a href="https://msdn.microsoft.com/a7ae0409-e89d-400a-a601-edc8e6e3fbcc">ICDecompressEx</a>, j, <a href="https://msdn.microsoft.com/6a1aa686-7f3d-43be-baaa-d20ea4a33f9b">ICDecompressExQuery</a>, and <a href="https://msdn.microsoft.com/83db0e07-7e93-4c77-a017-68a30b1372ef">ICDecompressOpen</a> functions to obtain alternate formats.




## -see-also




<a href="https://msdn.microsoft.com/a7ae0409-e89d-400a-a601-edc8e6e3fbcc">ICDecompressEx</a>



<a href="https://msdn.microsoft.com/35277938-6fae-4207-8b91-439af2b481e8">ICDecompressExBegin</a>



<a href="https://msdn.microsoft.com/6a1aa686-7f3d-43be-baaa-d20ea4a33f9b">ICDecompressExQuery</a>



<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

