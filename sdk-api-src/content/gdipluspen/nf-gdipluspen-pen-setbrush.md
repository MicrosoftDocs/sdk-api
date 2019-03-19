---
UID: NF:gdipluspen.Pen.SetBrush
title: Pen::SetBrush (gdipluspen.h)
author: windows-sdk-content
description: The Pen::SetBrush method sets the Brush object that a pen uses to fill a line.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetBrush_brush_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setbrush.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Pen class [GDI+],SetBrush method, Pen.SetBrush, Pen::SetBrush, SetBrush, SetBrush method [GDI+], SetBrush method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetBrush_brush_, gdiplus._gdiplus_CLASS_Pen_SetBrush_brush_
ms.topic: method
req.header: gdipluspen.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Pen.SetBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Pen::SetBrush


## -description


The <b>Pen::SetBrush</b> method sets the <a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a> object that a pen uses to fill a line.


## -parameters




### -param brush [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a> object for the pen to use to fill a line. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534459(v=VS.85).aspx">HatchBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533811(v=VS.85).aspx">Using a Brush to Fill Shapes</a>
 

 

