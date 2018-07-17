---
UID: NF:gdiplusheaders.CustomLineCap.SetStrokeJoin
title: CustomLineCap::SetStrokeJoin
author: windows-sdk-content
description: The CustomLineCap::SetStrokeJoin method sets the style of line join for the stroke. The line join specifies how two lines that intersect within the GraphicsPath object that makes up the custom line cap are joined.
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_SetStrokeJoin_lineJoin_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\setstrokejoin.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CustomLineCap class [GDI+],SetStrokeJoin method, CustomLineCap.SetStrokeJoin, CustomLineCap::SetStrokeJoin, SetStrokeJoin, SetStrokeJoin method [GDI+], SetStrokeJoin method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_SetStrokeJoin_lineJoin_, gdiplus._gdiplus_CLASS_CustomLineCap_SetStrokeJoin_lineJoin_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - CustomLineCap.SetStrokeJoin
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# CustomLineCap::SetStrokeJoin


## -description


The <b>CustomLineCap::SetStrokeJoin</b> method sets the style of line join for the stroke. The line join specifies how two lines that intersect within the <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object that makes up the custom line cap are joined.


## -parameters




### -param lineJoin [in]

Type: <b><a href="https://msdn.microsoft.com/7fd13263-10c9-45b1-99b4-a8da574a26f3">LineJoin</a></b>

Element of the <a href="https://msdn.microsoft.com/7fd13263-10c9-45b1-99b4-a8da574a26f3">LineJoin</a> enumeration that specifies the line join that will be used for two lines that are drawn by the same pen and that have overlapping ends. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/bab33c8b-3203-4560-9e71-c112d528e20c">CustomLineCap</a>



<a href="https://msdn.microsoft.com/e72e402b-3cb7-4fc7-9050-ce00054da352">LineCap</a>



<a href="https://msdn.microsoft.com/7fd13263-10c9-45b1-99b4-a8da574a26f3">LineJoin</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>
 

 

