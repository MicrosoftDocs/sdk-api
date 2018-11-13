---
UID: NF:gdiplusstringformat.StringFormat.SetLineAlignment
title: StringFormat::SetLineAlignment
author: windows-sdk-content
description: The StringFormat::SetLineAlignment method sets the line alignment of this StringFormat object in relation to the origin of the layout rectangle.
old-location: gdiplus\_gdiplus_CLASS_StringFormat_SetLineAlignment_align_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\setlinealignment.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: SetLineAlignment, SetLineAlignment method [GDI+], SetLineAlignment method [GDI+],StringFormat class, StringFormat class [GDI+],SetLineAlignment method, StringFormat.SetLineAlignment, StringFormat::SetLineAlignment, _gdiplus_CLASS_StringFormat_SetLineAlignment_align_, gdiplus._gdiplus_CLASS_StringFormat_SetLineAlignment_align_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusstringformat.h
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
 - StringFormat.SetLineAlignment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# StringFormat::SetLineAlignment


## -description


The <b>StringFormat::SetLineAlignment</b> method sets the line alignment of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534510(v=VS.85).aspx">StringFormat</a> object in relation to the origin of the layout rectangle. The line alignment setting specifies how to align the string vertically in the layout rectangle. The layout rectangle is used to position the displayed string.


## -parameters




### -param align [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534177(v=VS.85).aspx">StringAlignment</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534177(v=VS.85).aspx">StringAlignment</a> enumeration that specifies how to align a string in reference to the layout rectangle. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534437(v=VS.85).aspx">Font</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534508(v=VS.85).aspx">SolidBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534177(v=VS.85).aspx">StringAlignment</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534510(v=VS.85).aspx">StringFormat</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534181(v=VS.85).aspx">StringFormatFlags</a>
 

 

