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

# SetWindowOrgEx function


## -description


The <b>SetWindowOrgEx</b> function specifies which window point maps to the viewport origin (0,0).


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x

TBD


### -param y

TBD


### -param lppt

TBD




#### - X [in]

The x-coordinate, in logical units, of the new window origin.


#### - Y [in]

The y-coordinate, in logical units, of the new window origin.


#### - lpPoint [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that receives the previous origin of the window, in logical units. If <i>lpPoint</i> is <b>NULL</b>, this parameter is not used.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



This helps define the mapping from the logical coordinate space (also known as a <i>window</i>) to the device coordinate space (the <i>viewport</i>). <b>SetWindowOrgEx</b> specifies which logical point maps to the device point (0,0). It has the effect of shifting the axes so that the logical point (0,0) no longer refers to the upper-left corner.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
//map the logical point (xWinOrg, yWinOrg) to the device point (0,0) 
SetWindowOrgEx (hdc, xWinOrg, yWinOrg, NULL)
</pre>
</td>
</tr>
</table></span></div>
This is related to the <a href="https://msdn.microsoft.com/d3b6326e-9fec-42a1-8d2e-d1ad4fcc79a4">SetViewportOrgEx</a> function. Generally, you will use one function or the other, but not both. Regardless of your use of <b>SetWindowOrgEx</b> and <b>SetViewportOrgEx</b>, the device point (0,0) is always the upper-left corner.




## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/6e6c7090-edf4-46a3-8bcd-10a00c0cf847">GetViewportOrgEx</a>



<a href="https://msdn.microsoft.com/9579ed10-6d4c-4724-af8b-22cab5b6ff5e">GetWindowOrgEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>



<a href="https://msdn.microsoft.com/d3b6326e-9fec-42a1-8d2e-d1ad4fcc79a4">SetViewportOrgEx</a>
 

 

