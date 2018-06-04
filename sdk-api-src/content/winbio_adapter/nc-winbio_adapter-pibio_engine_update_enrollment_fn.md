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

# PIBIO_ENGINE_UPDATE_ENROLLMENT_FN callback function


## -description


Called by the Windows Biometric Framework to add the current feature set to the enrollment object.


## -parameters




### -param Pipeline [in, out]

Pointer to a <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param RejectDetail [out]

Pointer to a <b>WINBIO_REJECT_DETAIL</b> value that receives  additional information about the failure to update the enrollment object. If the update succeeds, this value should be set to zero.


## -returns



This function must return one of the following <b>HRESULT</b> values.

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
The last update succeeded and no additional feature sets are required to complete the template.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A mandatory pointer parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b> WINBIO_E_BAD_CAPTURE</b></b></dt>
</dl>
</td>
<td width="60%">
The feature set did not meet the internal enrollment requirements of the engine adapter. Further information about the failure is specified by the <i>RejectDetail</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
There is no enrollment in progress on this biometric unit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_I_MORE_DATA</b></b></dt>
</dl>
</td>
<td width="60%">
The last update succeeded, but the engine adapter requires one or more additional feature sets before it can complete the enrollment template.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cd029d7e-e103-4bbb-aaf9-36f3043b941c">EngineAdapterGetEnrollmentStatus</a>



<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>
 

 

