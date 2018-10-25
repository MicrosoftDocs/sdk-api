---
UID: NF:gdiplusheaders.CustomLineCap.SetBaseInset
title: CustomLineCap::SetBaseInset
author: windows-sdk-content
description: The CustomLineCap::SetBaseInset method sets the base inset value of this custom line cap. This is the distance between the end of a line and the base cap.
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_SetBaseInset_inset_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\setbaseinset.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CustomLineCap class [GDI+],SetBaseInset method, CustomLineCap.SetBaseInset, CustomLineCap::SetBaseInset, SetBaseInset, SetBaseInset method [GDI+], SetBaseInset method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_SetBaseInset_inset_, gdiplus._gdiplus_CLASS_CustomLineCap_SetBaseInset_inset_
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
 - CustomLineCap.SetBaseInset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# CustomLineCap::SetBaseInset


## -description


The <b>CustomLineCap::SetBaseInset</b> method sets the base inset value of this custom line cap. This is the distance between the end of a line and the base cap.


## -parameters




### -param inset [in]

Type: <b>REAL</b>

Real number that specifies the distance, in units, from the base cap to the start of the line. If this value is greater than the length of the line, the behavior of this method is undefined. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.
                

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534432(v=VS.85).aspx">CustomLineCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534146(v=VS.85).aspx">LineCap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>
 

 

