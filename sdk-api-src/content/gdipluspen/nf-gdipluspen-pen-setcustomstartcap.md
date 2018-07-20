---
UID: NF:gdipluspen.Pen.SetCustomStartCap
title: Pen::SetCustomStartCap
author: windows-sdk-content
description: The Pen::SetCustomStartCap method sets the custom start cap for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetCustomStartCap_customCap_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setcustomstartcap.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: Pen class [GDI+],SetCustomStartCap method, Pen.SetCustomStartCap, Pen::SetCustomStartCap, SetCustomStartCap, SetCustomStartCap method [GDI+], SetCustomStartCap method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetCustomStartCap_customCap_, gdiplus._gdiplus_CLASS_Pen_SetCustomStartCap_customCap_
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Pen.SetCustomStartCap
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Pen::SetCustomStartCap


## -description


The <b>Pen::SetCustomStartCap</b> method sets the custom start cap for this 
			<a href="https://msdn.microsoft.com/library/ms534485(v=VS.85).aspx">Pen</a> object.


## -parameters




### -param customCap [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/ms534432(v=VS.85).aspx">CustomLineCap</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/library/ms534432(v=VS.85).aspx">CustomLineCap</a> object that specifies the custom start cap for this 
					<a href="https://msdn.microsoft.com/library/ms534485(v=VS.85).aspx">Pen</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/ms533850(v=VS.85).aspx">Drawing a Custom Dashed Line</a>



<a href="https://msdn.microsoft.com/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/library/ms535022(v=VS.85).aspx">Pen::GetCustomEndCap</a>



<a href="https://msdn.microsoft.com/library/ms535023(v=VS.85).aspx">Pen::GetCustomStartCap</a>



<a href="https://msdn.microsoft.com/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>
 

 

