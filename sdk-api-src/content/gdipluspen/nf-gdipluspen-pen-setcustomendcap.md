---
UID: NF:gdipluspen.Pen.SetCustomEndCap
title: Pen::SetCustomEndCap
author: windows-sdk-content
description: The Pen::SetCustomEndCap method sets the custom end cap for this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetCustomEndCap_customCap_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setcustomendcap.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
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
- apiref
: 
- COM
: 
- gdipluspen.h
: 
- Pen.SetCustomEndCap
: 
req.product: GDI+ 1.0
---

# Pen::SetCustomEndCap


## -description


The <b>Pen::SetCustomEndCap</b> method sets the custom end cap for this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


## -parameters




### -param customCap [in]

Type: <b>const <a href="https://msdn.microsoft.com/bab33c8b-3203-4560-9e71-c112d528e20c">CustomLineCap</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/bab33c8b-3203-4560-9e71-c112d528e20c">CustomLineCap</a> object that specifies the custom end cap for this 
					<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/0e75de3b-1006-4c8f-875c-eeb0782f24b0">Drawing a Custom Dashed Line</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/fcc0c624-d60a-4c77-b7d0-3921f0b49471">Pen::GetCustomEndCap</a>



<a href="https://msdn.microsoft.com/39a64e5c-d82b-4b0e-b851-db42996047a0">Pen::GetCustomStartCap</a>



<a href="https://msdn.microsoft.com/ba247773-7e9f-4130-a14c-42c3153e4da5">Pen::GetEndCap</a>



<a href="https://msdn.microsoft.com/23384bd0-94da-4c2a-9228-47cc0f0d18a7">Pen::SetCustomStartCap</a>



<a href="https://msdn.microsoft.com/ea29dcf3-7c3e-44bd-957b-0e7c46592de3">Pen::SetEndCap</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>
 

 

