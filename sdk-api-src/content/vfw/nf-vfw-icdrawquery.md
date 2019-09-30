---
UID: NF:vfw.ICDrawQuery
title: ICDrawQuery macro (vfw.h)
author: windows-sdk-content
description: The ICDrawQuery macro queries a rendering driver to determine if it can render data in a specific format. You can use this macro or explicitly call the ICM_DRAW_QUERY message.
old-location: multimedia\icdrawquery.htm
tech.root: Multimedia
ms.assetid: 5cd673e3-af82-4c24-b0d5-4c3cb7c7ab71
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICDrawQuery, ICDrawQuery macro [Windows Multimedia], _win32_ICDrawQuery, multimedia.icdrawquery, vfw/ICDrawQuery
ms.topic: macro
f1_keywords: 
 - "vfw/ICDrawQuery"
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
 - ICDrawQuery
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICDrawQuery macro


## -description



The <b>ICDrawQuery</b> macro queries a rendering driver to determine if it can render data in a specific format. You can use this macro or explicitly call the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/icm-draw-query">ICM_DRAW_QUERY</a> message.




## -parameters




### -param hic

Handle to a driver. 


### -param lpbiInput

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure containing the input format. 


## -remarks



This macro differs from the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-icdrawbegin">ICDrawBegin</a> macro in that it queries the driver in a general sense. <b>ICDrawBegin</b> determines if the driver can draw the data using the specified format under specific conditions, such as stretching the image.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-macros">Video Compression Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/video-compression-manager">Video Compression Manager</a>
 

 

