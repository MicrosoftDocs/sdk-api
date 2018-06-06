---
UID: NF:vfw.ICDrawRealize
title: ICDrawRealize macro
author: windows-sdk-content
description: The ICDrawRealize macro notifies a rendering driver to realize its drawing palette while drawing. You can use this macro or explicitly call the ICM_DRAW_REALIZE message.
old-location: multimedia\icdrawrealize.htm
old-project: Multimedia
ms.assetid: b6605223-ce66-49fc-bfa7-6e3dd98e214a
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ICDrawRealize, ICDrawRealize macro [Windows Multimedia], _win32_ICDrawRealize, multimedia.icdrawrealize, vfw/ICDrawRealize
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
 - ICDrawRealize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# ICDrawRealize macro


## -description



The <b>ICDrawRealize</b> macro notifies a rendering driver to realize its drawing palette while drawing. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/501540cd-41e2-4f80-abf8-2ec2179970a9">ICM_DRAW_REALIZE</a> message.




## -parameters




### -param hic

Handle to a driver. 


### -param hdc

Handle of the DC used to realize the palette. 


### -param fBackground

Background flag. Specify <b>TRUE</b> to realize the palette as a background task or <b>FALSE</b> to realize the palette in the foreground. 


## -remarks



Drivers need to respond to this message only if the drawing palette is different from the decompressed palette.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

