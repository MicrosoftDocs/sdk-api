---
UID: NF:gdiplusheaders.Region.IsEmpty
title: Region::IsEmpty
author: windows-sdk-content
description: The Region::IsEmpty method determines whether this region is empty.
old-location: gdiplus\_gdiplus_CLASS_Region_IsEmpty_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\isempty.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IsEmpty, IsEmpty method [GDI+], IsEmpty method [GDI+],Region class, Region class [GDI+],IsEmpty method, Region.IsEmpty, Region::IsEmpty, _gdiplus_CLASS_Region_IsEmpty_g_, gdiplus._gdiplus_CLASS_Region_IsEmpty_g_
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
 - Region.IsEmpty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Region::IsEmpty


## -description


The <b>Region::IsEmpty</b> method determines whether this region is empty.


## -parameters




### -param g [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If this region is empty, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534771(v=VS.85).aspx">Region::IsInfinite</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534772(v=VS.85).aspx">Region::MakeEmpty</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534773(v=VS.85).aspx">Region::MakeInfinite</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>
 

 

