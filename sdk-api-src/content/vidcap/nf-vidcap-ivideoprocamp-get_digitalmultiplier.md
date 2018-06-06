---
UID: NF:vidcap.IVideoProcAmp.get_DigitalMultiplier
title: IVideoProcAmp::get_DigitalMultiplier
author: windows-sdk-content
description: The get_DigitalMultiplier method returns the camera's digital zoom level.
old-location: dshow\ivideoprocamp_get_digitalmultiplier.htm
old-project: DirectShow
ms.assetid: 0b7ab1a3-193c-4682-af35-ae0cc5f28f45
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVideoProcAmp interface [DirectShow],get_DigitalMultiplier method, IVideoProcAmp.get_DigitalMultiplier, IVideoProcAmp::get_DigitalMultiplier, IVideoProcAmpget_DigitalMultiplier, dshow.ivideoprocamp_get_digitalmultiplier, get_DigitalMultiplier, get_DigitalMultiplier method [DirectShow], get_DigitalMultiplier method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_DigitalMultiplier
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IVideoProcAmp.get_DigitalMultiplier
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVideoProcAmp::get_DigitalMultiplier


## -description


The <code>get_DigitalMultiplier</code> method returns the camera's digital zoom level.


## -parameters




### -param pValue [out]

Receives the digital zoom multiplier.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/42876f3b-d2b9-4ddb-85c0-80f5177eef6b">VideoProcAmpFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Digital zoom is applied after the image is captured. The effect of digital zoom is to multiply the optical magnification by a factor <i>m</i>, which can be calculated as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
m = ( (Z'cur - Z'min) * (m-max - 1) ) / (Z'max - Z'min) ) + 1
</pre>
</td>
</tr>
</table></span></div>
where

<ul>
<li>
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Z'cur</pre>
</td>
</tr>
</table></span></div> = Current digital zoom level.</li>
<li>
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Z'min</pre>
</td>
</tr>
</table></span></div>, <div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Z'max</pre>
</td>
</tr>
</table></span></div> = Minimum and maximum digital zoom. See <a href="https://msdn.microsoft.com/8a8a5f72-d51f-4f5a-95e4-ac8d1ac1b24f">IVideoProcAmp::getRange_DigitalMultiplier</a>.</li>
<li>
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>m-max</pre>
</td>
</tr>
</table></span></div> = Maximum digital magnification. See KSPROPERTY_VIDEOPROCAMP_DIGITAL_MULTIPLIER_LIMIT, documented in the Windows DDK.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/de566705-1f4b-4ffa-932d-a52521e6963b">ICameraControl::get_FocalLengths</a>



<a href="https://msdn.microsoft.com/efaef34a-688a-4c7d-b8ee-e0f52468e355">IVideoProcAmp Interface</a>
 

 

