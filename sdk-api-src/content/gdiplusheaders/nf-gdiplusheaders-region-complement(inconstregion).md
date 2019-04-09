---
UID: NF:gdiplusheaders.Region.Complement(IN const Region)
title: Region::Complement(IN const Region) (gdiplusheaders.h)
author: windows-sdk-content
description: The Region::Complement method updates this region to the portion of another region that does not intersect this region.
old-location: gdiplus\_gdiplus_CLASS_Region_Complement_region_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regioncomplementmethods\complement_18region.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Complement, Complement method [GDI+], Complement method [GDI+],Region class, Region class [GDI+],Complement method, Region.Complement, Region.Complement(IN const Region), Region.Complement(const Region*), Region::Complement, Region::Complement(IN const Region), _gdiplus_CLASS_Region_Complement_region_, gdiplus._gdiplus_CLASS_Region_Complement_region_
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
 - Region.Complement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Region::Complement(IN const Region)


## -description


The <b>Region::Complement</b> method updates this region to the portion of another region that does not intersect this region.


## -parameters




### -param region [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>object to use to update this 
					<b>Region</b>object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534501(v=VS.85).aspx">Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>
 

 

