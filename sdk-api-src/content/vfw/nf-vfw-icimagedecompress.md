---
UID: NF:vfw.ICImageDecompress
title: ICImageDecompress function
author: windows-sdk-content
description: The ICImageDecompress function decompresses an image without using initialization functions.
old-location: multimedia\icimagedecompress.htm
tech.root: Multimedia
ms.assetid: 8d27f0bd-9db5-482d-9000-75ad04762a67
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ICImageDecompress, ICImageDecompress function [Windows Multimedia], _win32_ICImageDecompress, multimedia.icimagedecompress, vfw/ICImageDecompress
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
 - ICImageDecompress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICImageDecompress function


## -description



The <b>ICImageDecompress</b> function decompresses an image without using initialization functions.




## -parameters




### -param hic

Handle to a decompressor opened with the <a href="https://msdn.microsoft.com/2637b6ef-2324-40db-99e4-773fcb6fdbf6">ICOpen</a> function. Specify <b>NULL</b> to have VCM select an appropriate decompressor for the compressed image.


### -param uiFlags

Reserved; must be zero.


### -param lpbiIn

Compressed input data format.


### -param lpBits

Pointer to input data bits to compress. The data bits exclude header and format information.


### -param lpbiOut

Decompressed output format. Specify <b>NULL</b> to let decompressor use an appropriate format.


## -returns



Returns a handle to an uncompressed DIB in the CF_DIB format if successful or <b>NULL</b> otherwise. Image data follows the format header.




## -remarks



To obtain the format information from the <b>LPBITMAPINFOHEADER</b> structure, use the <b>GlobalLock</b> function to lock the data. Use the <b>GlobalFree</b> function to free the DIB when you are finished.




## -see-also




<a href="https://msdn.microsoft.com/193961a5-b882-4769-bce7-a53d625fc9dd">Video Compression Functions</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

