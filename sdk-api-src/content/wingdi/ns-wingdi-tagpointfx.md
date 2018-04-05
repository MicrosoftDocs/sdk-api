---
UID: NS:wingdi.tagPOINTFX
title: tagPOINTFX
author: windows-driver-content
description: The POINTFX structure contains the coordinates of points that describe the outline of a character in a TrueType font.
old-location: gdi\pointfx.htm
old-project: gdi
ms.assetid: a8736c6c-7944-42ed-811c-308f41f1ab2f
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPPOINTFX, LPPOINTFX, LPPOINTFX structure pointer [Windows GDI], POINTFX, POINTFX structure [Windows GDI], _win32_POINTFX_str, gdi.pointfx, tagPOINTFX, wingdi/LPPOINTFX, wingdi/POINTFX"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: POINTFX, *LPPOINTFX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wingdi.h
api_name:
-	POINTFX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagPOINTFX structure


## -description



The <b>POINTFX</b> structure contains the coordinates of points that describe the outline of a character in a TrueType font.




## -struct-fields




### -field x

The x-component of a point on the outline of a TrueType character.


### -field y

The y-component of a point on the outline of a TrueType character.


## -remarks



The <b>POINTFX</b> structure is a member of the <a href="https://msdn.microsoft.com/59a26aec-786e-471b-8e08-ddffb04874d6">TTPOLYCURVE</a> and <a href="https://msdn.microsoft.com/eea54aeb-7847-4393-87fa-86de93017be8">TTPOLYGONHEADER</a> structures. Values in the <b>POINTFX</b> structure are specified in device units.




## -see-also




<a href="https://msdn.microsoft.com/b1d94060-e822-447f-82ba-fd1cf2ddaa3b">FIXED</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/59a26aec-786e-471b-8e08-ddffb04874d6">TTPOLYCURVE</a>



<a href="https://msdn.microsoft.com/eea54aeb-7847-4393-87fa-86de93017be8">TTPOLYGONHEADER</a>
 

 

