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

# ICameraControl::get_FocalLengths


## -description


The <code>get_FocalLengths</code> method returns the focal lengths of the camera lenses.


## -parameters




### -param plOcularFocalLength [out]

Receives the ocular focal length.


### -param plObjectiveFocalLengthMin [out]

Receives the minimum objective focal length.


### -param plObjectiveFocalLengthMax [out]

Receives the maximum objective focal length.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



In a two-lens camera, the objective lens is closer to the subject, and the ocular lens is closer to the camera. The ocular focal length is fixed. If the camera has an optical zoom, the objective focal length can vary within a fixed range. Magnification is calculated as the ratio of objective/ocular focal length. Because the magnification is expressed as a ratio, it has no units. Therefore, the units for the focal length are not defined by this interface.

If the camera supports optical zooming, the current zoom level is expressed as integer values between a range <i>Zmin</i> and <i>Zmax</i>. The objective focal length can then be calculated as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
Lcur = ( ( (Zcur - Zmin) * (Lmax - Lmin) ) / (Zmax - Zmin) ) + Lmin
</pre>
</td>
</tr>
</table></span></div>
where:

<ul>
<li>
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Lcur</pre>
</td>
</tr>
</table></span></div> = Current objective focal length.</li>
<li>
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Lmin</pre>
</td>
</tr>
</table></span></div>, <div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Lmax</pre>
</td>
</tr>
</table></span></div> = Minimum and maximum objective focal length.</li>
<li>
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Zcur</pre>
</td>
</tr>
</table></span></div> = Current zoom setting. See <a href="https://msdn.microsoft.com/7c1fe500-bccf-46ed-bcd9-f65b25e8ccb7">ICameraControl::get_Zoom</a>.</li>
<li>
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Zmin</pre>
</td>
</tr>
</table></span></div>, <div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Zmax</pre>
</td>
</tr>
</table></span></div> = Minimum and maximum zoom setting. See <a href="https://msdn.microsoft.com/93a81b65-4b63-45c9-b065-f4aa5cf2e4ae">ICameraControl::getRange_Zoom</a>.</li>
</ul>
From <div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Lcur</pre>
</td>
</tr>
</table></span></div>, you can calculate the magnification.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

