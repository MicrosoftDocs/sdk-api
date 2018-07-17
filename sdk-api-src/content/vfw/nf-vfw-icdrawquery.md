---
UID: NF:vfw.ICDrawQuery
title: ICDrawQuery macro
author: windows-sdk-content
description: The ICDrawQuery macro queries a rendering driver to determine if it can render data in a specific format. You can use this macro or explicitly call the ICM_DRAW_QUERY message.
old-location: multimedia\icdrawquery.htm
old-project: Multimedia
ms.assetid: 5cd673e3-af82-4c24-b0d5-4c3cb7c7ab71
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ICDrawQuery, ICDrawQuery macro [Windows Multimedia], _win32_ICDrawQuery, multimedia.icdrawquery, vfw/ICDrawQuery
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - ICDrawQuery
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICDrawQuery macro


## -description



The <b>ICDrawQuery</b> macro queries a rendering driver to determine if it can render data in a specific format. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/b829a04b-c1be-47c6-96e9-a6dc6f802811">ICM_DRAW_QUERY</a> message.




## -parameters




### -param hic

Handle to a driver. 


### -param lpbiInput

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the input format. 


## -remarks



This macro differs from the <a href="https://msdn.microsoft.com/52a43888-9839-45a3-b139-e84943c345c2">ICDrawBegin</a> macro in that it queries the driver in a general sense. <b>ICDrawBegin</b> determines if the driver can draw the data using the specified format under specific conditions, such as stretching the image.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

