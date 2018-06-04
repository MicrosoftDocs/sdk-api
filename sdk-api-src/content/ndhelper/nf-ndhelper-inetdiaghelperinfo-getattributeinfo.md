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

# INetDiagHelperInfo::GetAttributeInfo


## -description


The <b>GetAttributeInfo</b> method retrieves the list of key parameters needed by the Helper Class Extension.


## -parameters




### -param pcelt [out]

A pointer to a count of elements in the array pointed to by <i>pprgAttributeInfos</i>.


### -param pprgAttributeInfos [out]

A pointer to an array of <a href="https://msdn.microsoft.com/a4de3031-7199-4537-a97e-f33059383d6b">HelperAttributeInfo</a> structures that contain helper class key parameters.


## -returns



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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters has not been provided correctly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges to perform the diagnosis or repair operation.

</td>
</tr>
</table>
 

Helper Class Extensions may return HRESULTS that are specific to the diagnoses or repairs.




## -remarks



The key parameter list is used by NDF to determine whether enough information is available for the extension to perform diagnosis.  If the hypothesis to call the extension lacks a key attribute, the extension will not be called.  Optional attributes will not be returned by this call.




## -see-also




<a href="https://msdn.microsoft.com/815e2338-0055-4078-a9a5-197db449c33d">INetDiagHelperInfo</a>
 

 

