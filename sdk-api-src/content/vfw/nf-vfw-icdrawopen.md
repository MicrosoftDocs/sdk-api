---
UID: NF:vfw.ICDrawOpen
title: ICDrawOpen macro
author: windows-sdk-content
description: The ICDrawOpen macro opens a driver that can draw images with the specified format.
old-location: multimedia\icdrawopen.htm
tech.root: Multimedia
ms.assetid: b625a5f7-8212-4339-a1a6-37736def40a0
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICDrawOpen, ICDrawOpen macro [Windows Multimedia], _win32_ICDrawOpen, multimedia.icdrawopen, vfw/ICDrawOpen
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
 - ICDrawOpen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDrawOpen macro


## -description



The <b>ICDrawOpen</b> macro opens a driver that can draw images with the specified format.




## -parameters




### -param fccType

Four-character code indicating the type of driver to open. For video streams, the value of this parameter is "VIDC" or ICTYPE_VIDEO. 


### -param fccHandler

Four-character code indicating the preferred stream handler to use. Typically, this information is stored in the stream header in an AVI file. 


### -param lpbiIn

Pointer to the structure defining the input format. A driver handle will not be returned unless it can decompress this format. For images, this parameter refers to a <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a> structure. 


## -remarks



The <b>ICDrawOpen</b> macro is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define ICDrawOpen(fccType, fccHandler, lpbiIn) \
    ICLocate(fccType, fccHandler, lpbiIn, NULL, ICMODE_DRAW); 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

