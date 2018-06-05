---
UID: NF:gdipluspen.Pen.SetLineCap
title: Pen::SetLineCap
author: windows-sdk-content
description: The Pen::SetLineCap method sets the cap styles for the start, end, and dashes in a line drawn with this pen.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetLineCap_startCap_endCap_dashCap_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setlinecap.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Pen class [GDI+],SetLineCap method, Pen.SetLineCap, Pen::SetLineCap, SetLineCap, SetLineCap method [GDI+], SetLineCap method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetLineCap_startCap_endCap_dashCap_, gdiplus._gdiplus_CLASS_Pen_SetLineCap_startCap_endCap_dashCap_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WmfPlaceableFileHeader
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Pen.SetLineCap
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Pen::SetLineCap


## -description


The <b>Pen::SetLineCap</b> method sets the cap styles for the start, end, and dashes in a line drawn with this pen.


## -parameters




### -param startCap [in]

Type: <b><a href="https://msdn.microsoft.com/e72e402b-3cb7-4fc7-9050-ce00054da352">LineCap</a></b>

Element of the <a href="https://msdn.microsoft.com/e72e402b-3cb7-4fc7-9050-ce00054da352">LineCap</a> enumeration that specifies the start cap of a line. 


### -param endCap [in]

Type: <b><a href="https://msdn.microsoft.com/e72e402b-3cb7-4fc7-9050-ce00054da352">LineCap</a></b>

Element of the <a href="https://msdn.microsoft.com/e72e402b-3cb7-4fc7-9050-ce00054da352">LineCap</a> enumeration that specifies the end cap of a line. 


### -param dashCap [in]

Type: <b><a href="https://msdn.microsoft.com/8e96f7c2-237e-4172-8e3c-62d47627b430">DashCap</a></b>

Element of the 
					<a href="https://msdn.microsoft.com/8e96f7c2-237e-4172-8e3c-62d47627b430">DashCap</a> enumeration that specifies the start and end caps of the dashes in a dashed line. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/c9d90114-3913-486c-a808-b08dd473d9a1">Drawing a Line with Line Caps</a>



<a href="https://msdn.microsoft.com/e72e402b-3cb7-4fc7-9050-ce00054da352">LineCap</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/ba247773-7e9f-4130-a14c-42c3153e4da5">Pen::GetEndCap</a>



<a href="https://msdn.microsoft.com/4024524a-f139-4ec5-8788-b071658b8374">Pen::GetStartCap</a>



<a href="https://msdn.microsoft.com/d7be905c-92fe-4a7e-9422-f60912461dc9">Pen::SetCustomEndCap</a>



<a href="https://msdn.microsoft.com/23384bd0-94da-4c2a-9228-47cc0f0d18a7">Pen::SetCustomStartCap</a>



<a href="https://msdn.microsoft.com/ea29dcf3-7c3e-44bd-957b-0e7c46592de3">Pen::SetEndCap</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>
 

 

