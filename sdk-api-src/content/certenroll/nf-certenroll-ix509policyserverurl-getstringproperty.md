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

# IX509PolicyServerUrl::GetStringProperty


## -description


The <b>GetStringProperty</b> method retrieves the certificate enrollment policy (CEP) server ID or the display name of the CEP server.


## -parameters




### -param propertyId [in]

A <a href="https://msdn.microsoft.com/7b2f898d-9730-4f86-a7b2-dd625889c00a">PolicyServerUrlPropertyID</a> value that specifies the string to retrieve. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PsPolicyID"></a><a id="pspolicyid"></a><a id="PSPOLICYID"></a><dl>
<dt><b>PsPolicyID</b></dt>
</dl>
</td>
<td width="60%">
Retrieve an ID string for the policy server.

</td>
</tr>
<tr>
<td width="40%"><a id="PsFriendlyName"></a><a id="psfriendlyname"></a><a id="PSFRIENDLYNAME"></a><dl>
<dt><b>PsFriendlyName</b></dt>
</dl>
</td>
<td width="60%">
Retrieve a display name for the policy server.

</td>
</tr>
</table>
 


### -param ppValue [out, retval]

Pointer to a <b>BSTR</b> variable that receives the property value.


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
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The property value cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>propertyId</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory could not be allocated for the return value.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ad9d61ec-f607-4f71-ad8a-28d821e29c27">IX509PolicyServerUrl</a>
 

 

