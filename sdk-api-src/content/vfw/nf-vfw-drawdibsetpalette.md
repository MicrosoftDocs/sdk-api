---
UID: NF:vfw.DrawDibSetPalette
title: DrawDibSetPalette function
author: windows-sdk-content
description: The DrawDibSetPalette function sets the palette used for drawing DIBs.
old-location: multimedia\drawdibsetpalette.htm
tech.root: Multimedia
ms.assetid: 196c4409-024a-41e4-b553-e3337c936f19
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: DrawDibSetPalette, DrawDibSetPalette function [Windows Multimedia], _win32_DrawDibSetPalette, multimedia.drawdibsetpalette, vfw/DrawDibSetPalette
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/9ba47b8d-5328-477e-9272-21e897e54348">DrawDib Functions</a>
 

 

