---
UID: NF:vfw.DrawDibSetPalette
title: DrawDibSetPalette function (vfw.h)
author: windows-sdk-content
description: The DrawDibSetPalette function sets the palette used for drawing DIBs.
old-location: multimedia\drawdibsetpalette.htm
tech.root: Multimedia
ms.assetid: 196c4409-024a-41e4-b553-e3337c936f19
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrawDibSetPalette, DrawDibSetPalette function [Windows Multimedia], _win32_DrawDibSetPalette, multimedia.drawdibsetpalette, vfw/DrawDibSetPalette
ms.topic: function
f1_keywords: 
 - "vfw/DrawDibSetPalette"
dev_langs:
 - c++
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
 - DrawDibSetPalette
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DrawDibSetPalette function


## -description



The <b>DrawDibSetPalette</b> function sets the palette used for drawing DIBs.




## -parameters




### -param hdd

Handle to a DrawDib DC.


### -param hpal

Handle to the palette. Specify <b>NULL</b> to use the default palette.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/drawdib-functions">DrawDib Functions</a>
 

 

