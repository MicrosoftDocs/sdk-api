---
UID: NE:strmif.tagDVD_PARENTAL_LEVEL
title: tagDVD_PARENTAL_LEVEL
author: windows-driver-content
description: Identifies flags for the generic parental levels defined in the DVD specification.
old-location: dshow\dvd_parental_level.htm
old-project: DirectShow
ms.assetid: 0b18b5e8-f859-427e-b25f-2f4452492eb9
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: DVD_PARENTAL_LEVEL, DVD_PARENTAL_LEVEL , DVD_PARENTAL_LEVEL enumeration [DirectShow], DVD_PARENTAL_LEVELEnumeration, DVD_PARENTAL_LEVEL_1, DVD_PARENTAL_LEVEL_2, DVD_PARENTAL_LEVEL_3, DVD_PARENTAL_LEVEL_4, DVD_PARENTAL_LEVEL_5, DVD_PARENTAL_LEVEL_6, DVD_PARENTAL_LEVEL_7, DVD_PARENTAL_LEVEL_8, dshow.dvd_parental_level, strmif/DVD_PARENTAL_LEVEL, strmif/DVD_PARENTAL_LEVEL_1, strmif/DVD_PARENTAL_LEVEL_2, strmif/DVD_PARENTAL_LEVEL_3, strmif/DVD_PARENTAL_LEVEL_4, strmif/DVD_PARENTAL_LEVEL_5, strmif/DVD_PARENTAL_LEVEL_6, strmif/DVD_PARENTAL_LEVEL_7, strmif/DVD_PARENTAL_LEVEL_8, tagDVD_PARENTAL_LEVEL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVD_PARENTAL_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	DVD_PARENTAL_LEVEL
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# tagDVD_PARENTAL_LEVEL enumeration


## -description



Identifies flags for the generic parental levels defined in the DVD specification.




## -enum-fields




### -field DVD_PARENTAL_LEVEL_8

Parental level 8.


### -field DVD_PARENTAL_LEVEL_7

Parental level 7.


### -field DVD_PARENTAL_LEVEL_6

Parental level 6.


### -field DVD_PARENTAL_LEVEL_5

Parental level 5.


### -field DVD_PARENTAL_LEVEL_4

Parental level 4.


### -field DVD_PARENTAL_LEVEL_3

Parental level 3.


### -field DVD_PARENTAL_LEVEL_2

Parental level 2.


### -field DVD_PARENTAL_LEVEL_1

Parental level 1.


## -remarks



<b>DVD_PARENTAL_LEVEL_8</b> is the most restrictive level and <b>DVD_PARENTAL_LEVEL_1</b> is the least restrictive. The way in which the levels are interpreted or used varies from country/region to country/region. In the United States and Canada, the levels correspond to the Motion Picture Association of America (MPAA) rating levels as shown in the following table.

<table>
<tr>
<th>
              Parental level
            </th>
<th>
              Meaning
            </th>
</tr>
<tr>
<td>1</td>
<td>The rating is G, General.</td>
</tr>
<tr>
<td>3</td>
<td>The rating is PG, Parental Guidance Suggested.</td>
</tr>
<tr>
<td>4</td>
<td>The rating is PG-13, Parental Guidance Suggested, not recommended for those under 13.</td>
</tr>
<tr>
<td>6</td>
<td>The rating is R, Restricted.</td>
</tr>
<tr>
<td>7</td>
<td>The rating is NC-17.</td>
</tr>
</table>
 

This enumeration is used in the <a href="https://msdn.microsoft.com/00c9d1e5-1b1f-41b3-b06c-0b78e2d2db0b">IDvdInfo2::GetTitleParentalLevels</a> method.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/00c9d1e5-1b1f-41b3-b06c-0b78e2d2db0b">IDvdInfo2::GetTitleParentalLevels</a>
 

 

