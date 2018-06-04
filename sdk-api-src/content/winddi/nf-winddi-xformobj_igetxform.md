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

# XFORMOBJ_iGetXform function


## -description


The <b>XFORMOBJ_iGetXform</b> function downloads a transform to the driver.


## -parameters




### -param pxo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570618">XFORMOBJ</a> structure that defines the transform to be downloaded to the driver.


### -param pxform

Pointer to the buffer that is to receive the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570616">XFORML</a> structure. This parameter can be <b>NULL</b>.


## -returns



If an error occurs, the return value is DDI_ERROR. Otherwise, the return value is a complexity hint about the transform object. The value of this transform characterization can be one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GX_GENERAL</b></dt>
</dl>
</td>
<td width="60%">
Arbitrary 2 x 2 matrix and offset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GX_IDENTITY</b></dt>
</dl>
</td>
<td width="60%">
Identity matrix; no translation offset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GX_OFFSET</b></dt>
</dl>
</td>
<td width="60%">
Identity matrix; there is a translation offset.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>GX_SCALE</b></dt>
</dl>
</td>
<td width="60%">
Off-diagonal matrix elements are zero.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff570616">XFORML</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570618">XFORMOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570623">XFORMOBJ_bApplyXform</a>
 

 

