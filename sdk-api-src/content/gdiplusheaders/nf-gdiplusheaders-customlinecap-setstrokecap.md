---
UID: NF:gdiplusheaders.CustomLineCap.SetStrokeCap
title: CustomLineCap::SetStrokeCap
author: windows-sdk-content
description: The CustomLineCap::SetStrokeCap method sets the LineCap object used to start and end lines within the GraphicsPath object that defines this CustomLineCap object.
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_SetStrokeCap_strokeCap_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\setstrokecap.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CustomLineCap class [GDI+],SetStrokeCap method, CustomLineCap.SetStrokeCap, CustomLineCap::SetStrokeCap, SetStrokeCap, SetStrokeCap method [GDI+], SetStrokeCap method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_SetStrokeCap_strokeCap_, gdiplus._gdiplus_CLASS_CustomLineCap_SetStrokeCap_strokeCap_
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
 - CustomLineCap.SetStrokeCap
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# CustomLineCap::SetStrokeCap


## -description


The <b>CustomLineCap::SetStrokeCap</b> method sets the <a href="https://msdn.microsoft.com/en-us/library/ms534146(v=VS.85).aspx">LineCap</a> object used to start and end lines within the <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object that defines this <a href="https://msdn.microsoft.com/en-us/library/ms534432(v=VS.85).aspx">CustomLineCap</a> object.


## -parameters




### -param strokeCap [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534146(v=VS.85).aspx">LineCap</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534146(v=VS.85).aspx">LineCap</a> enumeration that specifies the line cap that will be used on the ends of the line to be drawn. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534432(v=VS.85).aspx">CustomLineCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534146(v=VS.85).aspx">LineCap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>
 

 

