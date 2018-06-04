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

# ImageAttributes::SetBrushRemapTable


## -description


The <b>ImageAttributes::SetBrushRemapTable</b> method sets the color remap table for the brush category.


## -parameters




### -param mapSize [in]

Type: <b>UINT</b>

<b>INT</b> that specifies the number of elements in the <i>map</i> array. 


### -param map [in]

Type: <b><a href="https://msdn.microsoft.com/7ecc81c9-f0b6-4352-8dbc-fdb416c0ddc8">ColorMap</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/7ecc81c9-f0b6-4352-8dbc-fdb416c0ddc8">ColorMap</a> structures. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



A color-remap table is an array of <a href="https://msdn.microsoft.com/7ecc81c9-f0b6-4352-8dbc-fdb416c0ddc8">ColorMap</a> structures. Each <b>ColorMap</b> structure has two <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> objects: one that specifies an old color and one that specifies a corresponding new color. During rendering, any color that matches one of the old colors in the remap table is changed to the corresponding new color.

Calling the <b>ImageAttributes::SetBrushRemapTable</b> method has the same effect as passing <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustTypeBrush</a> to the <a href="https://msdn.microsoft.com/87b63b0d-9071-4c7f-9ff6-14083092246a">ImageAttributes::SetRemapTable</a> method. The specified remap table applies to items in metafiles that are filled with a brush.


#### Examples



The following example creates an 
						<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object and sets its brush remap table so that red is converted to green.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
ImageAttributes imageAtt;
ColorMap cMap;
cMap.oldColor = Color(255, 255, 0, 0);  // red
cMap.newColor = Color(255, 0, 255, 0);  // green
imageAtt.SetBrushRemapTable(1, &amp;cMap);
				</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/7ecc81c9-f0b6-4352-8dbc-fdb416c0ddc8">ColorMap</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/7e018c5a-7933-43b6-b7b3-ee9daea16eb9">Recoloring</a>
 

 

