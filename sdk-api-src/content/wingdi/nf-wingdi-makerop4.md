---
UID: NF:wingdi.MAKEROP4
title: MAKEROP4 macro
author: windows-sdk-content
description: The MAKEROP4 macro creates a quaternary raster operation code for use with the MaskBlt function.
old-location: gdi\makerop4.htm
tech.root: gdi
ms.assetid: 9056df62-a636-49c7-9c86-aecc731e8c4f
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: MAKEROP4, MAKEROP4 macro [Windows GDI], _win32_MAKEROP4, gdi.makerop4, wingdi/MAKEROP4
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: wingdi.h
req.include-header: Windows.h
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
 - Wingdi.h
api_name:
 - MAKEROP4
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MAKEROP4 macro


## -description



The <b>MAKEROP4</b> macro creates a quaternary raster operation code for use with the <a href="https://msdn.microsoft.com/9fd6f0ce-a802-428d-9be5-a66afe39e9b7">MaskBlt</a> function. The macro takes two ternary raster operation codes as input, one for the foreground and one for the background, and packs their Boolean operation indexes into the high-order word of a 32-bit value. The low-order word of this value will be ignored.




## -parameters




### -param fore

The foreground ternary raster operation code.


### -param back

The background ternary raster operation code.


## -see-also




<a href="https://msdn.microsoft.com/8781bbf4-89fe-4212-b9df-e5b5cb07528c">Bitmap Macros</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/9fd6f0ce-a802-428d-9be5-a66afe39e9b7">MaskBlt</a>
 

 

