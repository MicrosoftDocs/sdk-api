---
UID: NF:gdiplusheaders.CustomLineCap.SetBaseCap
title: CustomLineCap::SetBaseCap
author: windows-driver-content
description: The CustomLineCap::SetBaseCap method sets the LineCap that appears as part of this CustomLineCap at the end of a line.
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_SetBaseCap_baseCap_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\setbasecap.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: CustomLineCap class [GDI+],SetBaseCap method, CustomLineCap.SetBaseCap, CustomLineCap::SetBaseCap, SetBaseCap, SetBaseCap method [GDI+], SetBaseCap method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_SetBaseCap_baseCap_, gdiplus._gdiplus_CLASS_CustomLineCap_SetBaseCap_baseCap_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	CustomLineCap.SetBaseCap
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# CustomLineCap::SetBaseCap


## -description


The <b>CustomLineCap::SetBaseCap</b> method sets the <a href="https://msdn.microsoft.com/e72e402b-3cb7-4fc7-9050-ce00054da352">LineCap</a> that appears as part of this <a href="https://msdn.microsoft.com/bab33c8b-3203-4560-9e71-c112d528e20c">CustomLineCap</a> at the end of a line.


## -parameters




### -param baseCap [in]

Type: <b><a href="https://msdn.microsoft.com/e72e402b-3cb7-4fc7-9050-ce00054da352">LineCap</a></b>

Element of the <a href="https://msdn.microsoft.com/e72e402b-3cb7-4fc7-9050-ce00054da352">LineCap</a> enumeration that specifies the line cap used on the ends of the line to be drawn. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/bab33c8b-3203-4560-9e71-c112d528e20c">CustomLineCap</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/e72e402b-3cb7-4fc7-9050-ce00054da352">LineCap</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>
 

 

