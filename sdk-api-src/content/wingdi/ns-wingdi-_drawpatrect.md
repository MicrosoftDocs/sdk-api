---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _DRAWPATRECT structure


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



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

