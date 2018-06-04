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

# NdfCreateIncident function


## -description


The <b>NdfCreateIncident</b> function is used internally by application developers to test the NDF functionality incorporated into their application.


## -parameters




### -param helperClassName [in]

Type: <b>LPCWSTR</b>

The name of the helper class to be used in the diagnoses of the incident.


### -param celt

Type: <b>ULONG</b>

A count of elements in the attributes array.


### -param attributes [in]

Type: <b><a href="https://msdn.microsoft.com/bff9303e-7fab-49af-b213-aa0a9c83676e">HELPER_ATTRIBUTE</a>*</b>

The applicable <a href="https://msdn.microsoft.com/bff9303e-7fab-49af-b213-aa0a9c83676e">HELPER_ATTRIBUTE</a> structure.


### -param handle [out]

Type: <b>NDFHANDLE*</b>

A handle to the Network Diagnostics Framework incident.


## -returns



Type: <b>HRESULT</b>

Possible return values include, but are not limited to, the following.

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
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NDF_E_BAD_PARAM</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>                NDF_E_NOHELPERCLASS</b></dt>
</dl>
</td>
<td width="60%">
<i>helperClassName</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5e5caf41-ca24-42e0-ac22-3b569400c383">NdfCloseIncident</a>



<a href="https://msdn.microsoft.com/c4cb2713-b656-47a8-9de7-9d33e864a811">NdfCreateWinSockIncident</a>



<a href="https://msdn.microsoft.com/b65f30c3-53d5-4282-8d38-5723772f15fc">NdfExecuteDiagnosis</a>
 

 

