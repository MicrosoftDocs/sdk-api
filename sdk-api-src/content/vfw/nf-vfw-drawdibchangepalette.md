---
UID: NF:vfw.DrawDibChangePalette
title: DrawDibChangePalette function (vfw.h)
author: windows-sdk-content
description: The DrawDibChangePalette function sets the palette entries used for drawing DIBs.
old-location: multimedia\drawdibchangepalette.htm
tech.root: Multimedia
ms.assetid: 8c94ecac-d12c-45c4-8a11-e17502bd7d5d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawDibChangePalette, DrawDibChangePalette function [Windows Multimedia], _win32_DrawDibChangePalette, multimedia.drawdibchangepalette, vfw/DrawDibChangePalette
ms.topic: function
f1_keywords: 
 - "vfw/DrawDibChangePalette"
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
 - DrawDibChangePalette
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



This function changes the physical palette only if the current DrawDib palette is realized by calling the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-drawdibrealize">DrawDibRealize</a> function.

If the color table is not changed, the next call to the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-drawdibdraw">DrawDibDraw</a> function that does not specify DDF_SAME_DRAW calls the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-drawdibbegin">DrawDibBegin</a> function implicitly.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/drawdib-functions">DrawDib Functions</a>
 

 

