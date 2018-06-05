---
UID: NF:vfw.ICDrawEnd
title: ICDrawEnd macro
author: windows-sdk-content
description: The ICDrawEnd macro notifies a rendering driver to decompress the current image to the screen and to release resources allocated for decompression and drawing. You can use this macro or explicitly call the ICM_DRAW_END message.
old-location: multimedia\icdrawend.htm
old-project: Multimedia
ms.assetid: efcb1913-edaf-454c-a317-c14349805a81
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ICDrawEnd, ICDrawEnd macro [Windows Multimedia], _win32_ICDrawEnd, multimedia.icdrawend, vfw/ICDrawEnd
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
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vfw.h
api_name:
-	ICDrawEnd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICDrawEnd macro


## -description



The <b>ICDrawEnd</b> macro notifies a rendering driver to decompress the current image to the screen and to release resources allocated for decompression and drawing. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/03910752-6122-4a5a-84ff-2cecf66cf439">ICM_DRAW_END</a> message.




## -parameters




### -param hic

Handle to a driver. 


## -remarks



The <a href="https://msdn.microsoft.com/e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8">ICM_DRAW_BEGIN</a> and <a href="https://msdn.microsoft.com/03910752-6122-4a5a-84ff-2cecf66cf439">ICM_DRAW_END</a> messages do not nest. If your driver receives <b>ICM_DRAW_BEGIN</b> before decompression is stopped with <b>ICM_DRAW_END</b>, it should restart decompression with new parameters.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

