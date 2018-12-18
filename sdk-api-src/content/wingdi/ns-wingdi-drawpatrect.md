---
UID: NS:wingdi._DRAWPATRECT
title: DRAWPATRECT
author: windows-sdk-content
description: The DRAWPATRECT structure defines a rectangle to be created.
old-location: gdi\drawpatrect.htm
tech.root: printdocs
ms.assetid: 8b374a0e-8ad0-40d4-a082-e90aff6336ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDRAWPATRECT, DRAWPATRECT, DRAWPATRECT structure [Windows GDI], PDRAWPATRECT, PDRAWPATRECT structure pointer [Windows GDI], _win32_DRAWPATRECT_str, gdi.drawpatrect, wingdi/DRAWPATRECT, wingdi/PDRAWPATRECT"
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - DRAWPATRECT
product: Windows
targetos: Windows
req.typenames: DRAWPATRECT, *PDRAWPATRECT
req.redist: 
---

# DRAWPATRECT structure


## -description



The <b>DRAWPATRECT</b> structure defines a rectangle to be created.




## -struct-fields




### -field ptPosition

The upper-left corner of the rectangle, in logical units.


### -field ptSize

The lower-right corner of the rectangle, in logical units.


### -field wStyle

The style of the rectangle. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>0</td>
<td>Black rectangle.</td>
</tr>
<tr>
<td>1</td>
<td>White rectangle.</td>
</tr>
<tr>
<td>2</td>
<td>Gray rectangle. Used with <b>wPattern</b>.</td>
</tr>
</table>
 


### -field wPattern

Amount of grayness of the rectangle, as a percentage (0-100). A value of 0 means a white rectangle and 100 means a black rectangle. This is only used when <b>wStyle</b> is 2.


## -remarks



This structure is used with the <a href="https://msdn.microsoft.com/5b8f1b44-4076-40d7-9e69-dc4cecaee597">DRAWPATTERNRECT</a> printer escape.




## -see-also




<a href="https://msdn.microsoft.com/5b8f1b44-4076-40d7-9e69-dc4cecaee597">DRAWPATTERNRECT</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>
 

 

