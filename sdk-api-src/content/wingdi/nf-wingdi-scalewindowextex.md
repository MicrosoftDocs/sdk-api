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

# ScaleWindowExtEx function


## -description


The <b>ScaleWindowExtEx</b> function modifies the window for a device context using the ratios formed by the specified multiplicands and divisors.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param xn

TBD


### -param xd

TBD


### -param yn

TBD


### -param yd

TBD


### -param lpsz

TBD




#### - Xdenom [in]

The amount by which to divide the current horizontal extent.


#### - Xnum [in]

The amount by which to multiply the current horizontal extent.


#### - Ydenom [in]

The amount by which to divide the current vertical extent.


#### - Ynum [in]

The amount by which to multiply the current vertical extent.


#### - lpSize [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure that receives the previous window extents, in logical units. If <i>lpSize</i> is <b>NULL</b>, this parameter is not used.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The window extents are modified as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
    xNewWE = (xOldWE * Xnum) / Xdenom 
    yNewWE = (yOldWE * Ynum) / Ydenom 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/17f41fcb-c9a4-4b7e-acde-73450044413e">GetWindowExtEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a>
 

 

