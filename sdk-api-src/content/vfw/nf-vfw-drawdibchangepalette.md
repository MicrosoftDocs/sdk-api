---
UID: NF:vfw.DrawDibChangePalette
title: DrawDibChangePalette function
author: windows-sdk-content
description: The DrawDibChangePalette function sets the palette entries used for drawing DIBs.
old-location: multimedia\drawdibchangepalette.htm
old-project: Multimedia
ms.assetid: 8c94ecac-d12c-45c4-8a11-e17502bd7d5d
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: DrawDibChangePalette, DrawDibChangePalette function [Windows Multimedia], _win32_DrawDibChangePalette, multimedia.drawdibchangepalette, vfw/DrawDibChangePalette
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msvfw32.dll
api_name:
 - DrawDibChangePalette
product: Windows
targetos: Windows
req.lib: Vfw32.lib
req.dll: Msvfw32.dll
req.irql: 
req.product: Windows UI
---

# DrawDibChangePalette function


## -description



The <b>DrawDibChangePalette</b> function sets the palette entries used for drawing DIBs.




## -parameters




### -param hdd

Handle to a DrawDib DC.


### -param iStart

Starting palette entry number.


### -param iLen

Number of palette entries.


### -param lppe

Pointer to an array of palette entries.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -remarks



This function changes the physical palette only if the current DrawDib palette is realized by calling the <a href="https://msdn.microsoft.com/4723c8a4-36af-4543-b6df-d51f68a3e94d">DrawDibRealize</a> function.

If the color table is not changed, the next call to the <a href="https://msdn.microsoft.com/b503fcd8-e928-4b3c-9ff5-96b88c5fb2f4">DrawDibDraw</a> function that does not specify DDF_SAME_DRAW calls the <a href="https://msdn.microsoft.com/89178e33-e440-49fe-9900-0baea229d289">DrawDibBegin</a> function implicitly.




## -see-also




<a href="https://msdn.microsoft.com/9ba47b8d-5328-477e-9272-21e897e54348">DrawDib Functions</a>
 

 

