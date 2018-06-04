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

# IWMResamplerProps::SetUserChannelMtx


## -description



Specifies the channel matrix.



## -parameters




### -param userChannelMtx [in]

Pointer to an array of floating-point values that represents a channel conversion matrix.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method is equivalent to setting the <a href="https://msdn.microsoft.com/2f2a82bd-f051-4b05-a9c8-37aa4403fab4">MFPKEY_WMRESAMP_CHANNELMTX</a> property, except that the matrix is represented differently:

<ul>
<li>Values are floating point.</li>
<li>The matrix is transposed.</li>
</ul>
To convert from the integer values given in the MFPKEY_WMRESAMP_CHANNELMTX property to floating-point values, use the following formula:

<code>(float)pow(10.0,((double)Coeff)/(65536.0*20.0))</code>

where <i>Coeff</i> is an integer coefficient.




## -see-also




<a href="https://msdn.microsoft.com/af3cec68-59a2-4b9d-a279-e5af46e9c38e">IWMResamplerProps Interface</a>
 

 

