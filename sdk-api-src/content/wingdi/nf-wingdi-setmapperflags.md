---
UID: NF:wingdi.SetMapperFlags
title: SetMapperFlags function
author: windows-driver-content
description: The SetMapperFlags function alters the algorithm the font mapper uses when it maps logical fonts to physical fonts.
old-location: gdi\setmapperflags.htm
old-project: gdi
ms.assetid: 74cfe0d3-0d20-4382-8e76-55a6e2323308
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: SetMapperFlags, SetMapperFlags function [Windows GDI], _win32_SetMapperFlags, gdi.setmapperflags, wingdi/SetMapperFlags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: FAX_TIME, *PFAX_TIME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	SetMapperFlags
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetMapperFlags function


## -description


The <b>SetMapperFlags</b> function alters the algorithm the font mapper uses when it maps logical fonts to physical fonts.


## -parameters




### -param hdc [in]

A handle to the device context that contains the font-mapper flag.


### -param flags

TBD




#### - dwFlag [in]

Specifies whether the font mapper should attempt to match a font's aspect ratio to the current device's aspect ratio. If bit zero is set, the mapper selects only matching fonts.


## -returns



If the function succeeds, the return value is the previous value of the font-mapper flag.

If the function fails, the return value is GDI_ERROR.




## -remarks



If the <i>dwFlag</i> parameter is set and no matching fonts exist, Windows chooses a new aspect ratio and retrieves a font that matches this ratio.

The remaining bits of the <i>dwFlag</i> parameter must be zero.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/3f2dd47d-08bf-4848-897f-5ae506fba342">GetAspectRatioFilterEx</a>
 

 

