---
UID: NF:gdipluspen.Pen.SetLineCap
title: Pen::SetLineCap
author: windows-sdk-content
description: The Pen::SetLineCap method sets the cap styles for the start, end, and dashes in a line drawn with this pen.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetLineCap_startCap_endCap_dashCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setlinecap.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Pen class [GDI+],SetLineCap method, Pen.SetLineCap, Pen::SetLineCap, SetLineCap, SetLineCap method [GDI+], SetLineCap method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetLineCap_startCap_endCap_dashCap_, gdiplus._gdiplus_CLASS_Pen_SetLineCap_startCap_endCap_dashCap_
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Pen.SetLineCap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Pen::SetLineCap


## -description


The <b>Pen::SetLineCap</b> method sets the cap styles for the start, end, and dashes in a line drawn with this pen.


## -parameters




### -param startCap [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534146(v=VS.85).aspx">LineCap</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534146(v=VS.85).aspx">LineCap</a> enumeration that specifies the start cap of a line. 


### -param endCap [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534146(v=VS.85).aspx">LineCap</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534146(v=VS.85).aspx">LineCap</a> enumeration that specifies the end cap of a line. 


### -param dashCap [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534102(v=VS.85).aspx">DashCap</a></b>

Element of the 
					<a href="https://msdn.microsoft.com/en-us/library/ms534102(v=VS.85).aspx">DashCap</a> enumeration that specifies the start and end caps of the dashes in a dashed line. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533852(v=VS.85).aspx">Drawing a Line with Line Caps</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534146(v=VS.85).aspx">LineCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535029(v=VS.85).aspx">Pen::GetEndCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535034(v=VS.85).aspx">Pen::GetStartCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535045(v=VS.85).aspx">Pen::SetCustomEndCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535046(v=VS.85).aspx">Pen::SetCustomStartCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535051(v=VS.85).aspx">Pen::SetEndCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>
 

 

