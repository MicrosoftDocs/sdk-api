---
UID: NF:vfw.ICDrawChangePalette
title: ICDrawChangePalette macro
author: windows-sdk-content
description: The ICDrawChangePalette macro notifies a rendering driver that the movie palette is changing. You can use this macro or explicitly call the ICM_DRAW_CHANGEPALETTE message.
old-location: multimedia\icdrawchangepalette.htm
tech.root: Multimedia
ms.assetid: 4b280b51-a45f-47e5-b54c-47dc4a6ca81c
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ICDrawChangePalette, ICDrawChangePalette macro [Windows Multimedia], _win32_ICDrawChangePalette, multimedia.icdrawchangepalette, vfw/ICDrawChangePalette
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
 - ICDrawChangePalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICDrawChangePalette macro


## -description



The <b>ICDrawChangePalette</b> macro notifies a rendering driver that the movie palette is changing. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/974fc0d8-d0c7-4a82-af84-68b53f753259">ICM_DRAW_CHANGEPALETTE</a> message.




## -parameters




### -param hic

Handle to a rendering driver. 


### -param lpbiInput

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the new format and optional color table. 


## -remarks



This message should be supported by installable rendering handlers that draw DIBs with an internal structure that includes a palette.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

