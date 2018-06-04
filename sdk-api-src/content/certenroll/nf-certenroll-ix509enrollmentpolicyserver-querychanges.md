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

# IX509EnrollmentPolicyServer::QueryChanges


## -description


The <b>QueryChanges</b> method retrieves a value that specifies whether the template or certification authority collections have changed in Active Directory.


## -parameters




### -param pValue [out, retval]

Pointer to a Boolean value that specifies whether the collections have changed.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOT_VALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
LoadOptionRegisterForADChanges was not specified in the <i>option</i> parameter of the <a href="https://msdn.microsoft.com/5b617c6e-91bc-4a22-acd6-41083102850a">LoadPolicy</a> method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pValue</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a> object has not been initialized.

</td>
</tr>
</table>
 




## -remarks



The <b>QueryChanges</b> method is relevant only when you specify <b>LoadOptionRegisterForADChanges</b> in the <i>option</i> parameter of the <a href="https://msdn.microsoft.com/5b617c6e-91bc-4a22-acd6-41083102850a">LoadPolicy</a> method. The method returns <b>VARIANT_TRUE</b> for either of the following cases:

<ul>
<li>The template collection in Active Directory has changed since the last time <a href="https://msdn.microsoft.com/52dd85aa-033b-43ab-9b71-1080f969bebc">GetTemplates</a> was called.</li>
<li>The certification authority collection in Active Directory has changed since the last time <a href="https://msdn.microsoft.com/37836fd1-e95a-4025-b268-f78a9113e568">GetCAs</a> was called.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a>
 

 

