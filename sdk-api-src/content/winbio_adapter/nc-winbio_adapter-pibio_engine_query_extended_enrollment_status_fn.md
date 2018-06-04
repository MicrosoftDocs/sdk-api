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

# PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN callback function


## -description


Called by the Windows Biometric Framework when a client application queries the <b>WINBIO_PROPERTY_EXTENDED_ENROLLMENT_STATUS</b>  property.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param EnrollmentStatus [out]

Pointer to the <a href="https://msdn.microsoft.com/2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B">WINBIO_EXTENDED_ENROLLMENT_STATUS</a> structure that contains the extended enrollment status information returned by this function.


### -param EnrollmentStatusSize [in]

The specified size in bytes of the extended enrollment status information.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Pipeline</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
The <i>EnrollmentStatusSize</i> parameter indicates that the output buffer is too small.

</td>
</tr>
</table>
 




## -remarks



Enrollment applications can request extended enrollment status information after each call to the <a href="https://msdn.microsoft.com/a50f0c9f-7b9c-4d80-b8fc-8b83bc333578">WinBioEnrollCapture</a> function.

If the biometric unit is not currently an enrollment template when this routine is called, the engine adapter should set the EnrollmentStatus.TemplateStatus field to <b>WINBIO_E_INVALID_OPERATION</b> and return <b>S_OK</b> as the value of the function.



