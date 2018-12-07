---
UID: NF:vfw.ICDecompressGetPalette
title: ICDecompressGetPalette macro
author: windows-sdk-content
description: The ICDecompressGetPalette macro requests that the video decompression driver supply the color table of the output BITMAPINFOHEADER structure. You can use this macro or explicitly call the ICM_DECOMPRESS_GET_PALETTE message.
old-location: multimedia\icdecompressgetpalette.htm
tech.root: Multimedia
ms.assetid: 433155ce-f9a1-408d-9caa-43a736fbdc67
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICDecompressGetPalette, ICDecompressGetPalette macro [Windows Multimedia], _win32_ICDecompressGetPalette, multimedia.icdecompressgetpalette, vfw/ICDecompressGetPalette
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
 - ICDecompressGetPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDecompressGetPalette macro


## -description



The <b>ICDecompressGetPalette</b> macro requests that the video decompression driver supply the color table of the output <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/f9fae9ab-9f69-44b6-bedb-f56f43845229">ICM_DECOMPRESS_GET_PALETTE</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


### -param lpbiInput

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure containing the input format. 


### -param lpbiOutput

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure to contain the color table. The space reserved for the color table is always at least 256 colors. You can specify zero for this parameter to return only the size of the color table. 


## -remarks



If <i>lpbiOutput</i> is nonzero, the driver sets the <b>biClrUsed</b> member of <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> to the number of colors in the color table. The driver fills the <b>bmiColors</b> members of <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> with the actual colors.

The driver should support this message only if it uses a palette other than the one specified in the input format.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

