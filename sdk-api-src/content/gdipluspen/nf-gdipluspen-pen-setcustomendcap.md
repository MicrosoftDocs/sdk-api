---
UID: NF:gdipluspen.Pen.SetCustomEndCap
title: Pen::SetCustomEndCap
author: windows-sdk-content
description: The Pen::SetCustomEndCap method sets the custom end cap for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetCustomEndCap_customCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setcustomendcap.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: Pen class [GDI+],SetCustomEndCap method, Pen.SetCustomEndCap, Pen::SetCustomEndCap, SetCustomEndCap, SetCustomEndCap method [GDI+], SetCustomEndCap method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetCustomEndCap_customCap_, gdiplus._gdiplus_CLASS_Pen_SetCustomEndCap_customCap_
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
 - Pen.SetCustomEndCap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Pen::SetCustomEndCap


## -description


The <b>Pen::SetCustomEndCap</b> method sets the custom end cap for this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object.


## -parameters




### -param customCap [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534432(v=VS.85).aspx">CustomLineCap</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/en-us/library/ms534432(v=VS.85).aspx">CustomLineCap</a> object that specifies the custom end cap for this 
					<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533850(v=VS.85).aspx">Drawing a Custom Dashed Line</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535022(v=VS.85).aspx">Pen::GetCustomEndCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535023(v=VS.85).aspx">Pen::GetCustomStartCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535029(v=VS.85).aspx">Pen::GetEndCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535046(v=VS.85).aspx">Pen::SetCustomStartCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535051(v=VS.85).aspx">Pen::SetEndCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>
 

 

