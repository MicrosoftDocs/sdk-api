---
UID: NF:gdipluspen.Pen.SetCustomEndCap
title: Pen::SetCustomEndCap (gdipluspen.h)
author: windows-sdk-content
description: The Pen::SetCustomEndCap method sets the custom end cap for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetCustomEndCap_customCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setcustomendcap.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],SetCustomEndCap method, Pen.SetCustomEndCap, Pen::SetCustomEndCap, SetCustomEndCap, SetCustomEndCap method [GDI+], SetCustomEndCap method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetCustomEndCap_customCap_, gdiplus._gdiplus_CLASS_Pen_SetCustomEndCap_customCap_
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
 - Pen.SetCustomEndCap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Pen::SetCustomEndCap


## -description


The <b>Pen::SetCustomEndCap</b> method sets the custom end cap for this 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.


## -parameters




### -param customCap [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a>*</b>

Pointer to a 
					<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a> object that specifies the custom end cap for this 
					<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-drawing-a-custom-dashed-line-use">Drawing a Custom Dashed Line</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getcustomendcap">Pen::GetCustomEndCap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getcustomstartcap">Pen::GetCustomStartCap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getendcap">Pen::GetEndCap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setcustomstartcap">Pen::SetCustomStartCap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setendcap">Pen::SetEndCap</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>
 

 

