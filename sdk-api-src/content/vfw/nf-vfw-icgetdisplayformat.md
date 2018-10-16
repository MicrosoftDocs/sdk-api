---
UID: NF:vfw.ICGetDisplayFormat
title: ICGetDisplayFormat function
author: windows-sdk-content
description: The ICGetDisplayFormat function determines the best format available for displaying a compressed image. The function also opens a compressor if a handle of an open compressor is not specified.
old-location: multimedia\icgetdisplayformat.htm
tech.root: Multimedia
ms.assetid: 4e588524-4105-4496-bc87-407abc45f598
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ICGetDisplayFormat, ICGetDisplayFormat function [Windows Multimedia], _win32_ICGetDisplayFormat, multimedia.icgetdisplayformat, vfw/ICGetDisplayFormat
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
 - ICGetDisplayFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICGetDisplayFormat function


## -description



The <b>ICGetDisplayFormat</b> function determines the best format available for displaying a compressed image. The function also opens a compressor if a handle of an open compressor is not specified.




## -parameters




### -param hic

Handle to the compressor to use. Specify <b>NULL</b> to have VCM select and open an appropriate compressor.
          


### -param lpbiIn

Pointer to <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the compressed format.
          


### -param lpbiOut

Pointer to a buffer to return the decompressed format. The buffer should be large enough for a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure and 256 color entries.
          


### -param BitDepth

Preferred bit depth, if nonzero.
          


### -param dx

Width multiplier to stretch the image. If this parameter is zero, that dimension is not stretched.
          


### -param dy

Height multiplier to stretch the image. If this parameter is zero, that dimension is not stretched.
          


## -returns



Returns a handle to a decompressor if successful or zero otherwise.
          




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

