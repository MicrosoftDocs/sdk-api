---
UID: NF:gdiplusheaders.Region.Exclude(IN const Region)
title: Region::Exclude(IN const Region)
author: windows-sdk-content
description: The Region::Exclude method updates this region to the portion of itself that does not intersect another region.
old-location: gdiplus\_gdiplus_CLASS_Region_Exclude_region_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regionexcludemethods\exclude_82region.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Exclude, Exclude method [GDI+], Exclude method [GDI+],Region class, Region class [GDI+],Exclude method, Region.Exclude, Region.Exclude(IN const Region), Region.Exclude(const Region*), Region::Exclude, Region::Exclude(IN const Region), _gdiplus_CLASS_Region_Exclude_region_, gdiplus._gdiplus_CLASS_Region_Exclude_region_
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
 - Region.Exclude
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- Region.Exclude
: 
req.product: GDI+ 1.0
---

# Region::Exclude(IN const Region)


## -description


The <b>Region::Exclude</b> method updates this region to the portion of itself that does not intersect another region.


## -parameters




### -param region [in]

Type: <b>const <a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a>object to use to update this 
					<b>Region</b>object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.



