---
UID: NS:winuser.tagDRAWTEXTPARAMS
title: tagDRAWTEXTPARAMS
author: windows-driver-content
description: The DRAWTEXTPARAMS structure contains extended formatting options for the DrawTextEx function.
old-location: gdi\drawtextparams.htm
old-project: gdi
ms.assetid: d3b89ce2-9a05-42af-b03e-24e1c4d6ef1d
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: "*LPDRAWTEXTPARAMS, DRAWTEXTPARAMS, DRAWTEXTPARAMS structure [Windows GDI], LPDRAWTEXTPARAMS, LPDRAWTEXTPARAMS structure pointer [Windows GDI], _win32_DRAWTEXTPARAMS_str, gdi.drawtextparams, tagDRAWTEXTPARAMS, winuser/DRAWTEXTPARAMS, winuser/LPDRAWTEXTPARAMS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winuser.h
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
req.typenames: DRAWTEXTPARAMS, *LPDRAWTEXTPARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winuser.h
api_name:
-	DRAWTEXTPARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagDRAWTEXTPARAMS structure


## -description



The <b>DRAWTEXTPARAMS</b> structure contains extended formatting options for the <a href="https://msdn.microsoft.com/77b9973b-77f1-4508-a021-52d61d576c23">DrawTextEx</a> function.




## -struct-fields




### -field cbSize

The structure size, in bytes.


### -field iTabLength

The size of each tab stop, in units equal to the average character width.


### -field iLeftMargin

The left margin, in units equal to the average character width.


### -field iRightMargin

The right margin, in units equal to the average character width.


### -field uiLengthDrawn

Receives the number of characters processed by <a href="https://msdn.microsoft.com/77b9973b-77f1-4508-a021-52d61d576c23">DrawTextEx</a>, including white-space characters. The number can be the <a href="https://msdn.microsoft.com/695fd0f9-abd4-4666-acad-2c409624ddc6">length of the string</a> or the index of the first line that falls below the drawing area. Note that <b>DrawTextEx</b> always processes the entire string if the DT_NOCLIP formatting flag is specified.


## -see-also




<a href="https://msdn.microsoft.com/77b9973b-77f1-4508-a021-52d61d576c23">DrawTextEx</a>



<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>
 

 

