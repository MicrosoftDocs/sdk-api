---
UID: NF:vfw.ICDecompressExQuery
title: ICDecompressExQuery function
author: windows-driver-content
description: The ICDecompressExQuery function determines if a decompressor can decompress data with a specific format.
old-location: multimedia\icdecompressexquery.htm
old-project: Multimedia
ms.assetid: 6a1aa686-7f3d-43be-baaa-d20ea4a33f9b
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ICDecompressExQuery, ICDecompressExQuery function [Windows Multimedia], _win32_ICDecompressExQuery, multimedia.icdecompressexquery, vfw/ICDecompressExQuery
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
req.typenames: VS_FIXEDFILEINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	ICDecompressExQuery
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICDecompressExQuery function


## -description



The <b>ICDecompressExQuery</b> function determines if a decompressor can decompress data with a specific format.




## -parameters




### -param hic

Handle to the decompressor to use.


### -param dwFlags

Reserved; do not use.


### -param lpbiSrc

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the format of the compressed data to decompress.


### -param lpSrc

Reserved; must be <b>NULL</b>.


### -param xSrc

The x-coordinate of the source rectangle for the DIB specified by <i>lpbiSrc</i>.


### -param ySrc

The y-coordinate of the source rectangle for the DIB specified by <i>lpbiSrc</i>.


### -param dxSrc

Width of the source rectangle.


### -param dySrc

Height of the source rectangle.


### -param lpbiDst

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the output format. If the value of this parameter is <b>NULL</b>, the function determines whether the input format is supported and this parameter is ignored.


### -param lpDst


            Pointer to a buffer that is large enough to contain the decompressed data.
          


### -param xDst


            The x-coordinate of the destination rectangle for the DIB specified by <i>lpbiDst</i>.
          


### -param yDst


            The y-coordinate of the destination rectangle for the DIB specified by <i>lpbiDst</i>.
          


### -param dxDst


            Width of the destination rectangle.
          


### -param dyDst


            Height of the destination rectangle.
          


## -returns




            Returns <b>ICERR_OK</b> if successful or an error otherwise.
          




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

