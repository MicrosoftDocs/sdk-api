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

# IFunctionInstanceCollectionQuery::AddPropertyConstraint


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Adds a property constraint to the query.

This method limits query results to only function instances with a property key (PKEY) matching the specified constraint.


## -parameters




### -param Key [in]

The property key (PKEY) for the constraint. For more information about PKEYs, see <a href="https://msdn.microsoft.com/76184645-82f5-46ef-8250-8f4276b2a105">Key Definitions</a>. 


### -param pv [in]

A <b>PROPVARIANT</b> used for the constraint. This type must match the PROPVARIANT type associated with <i>Key</i>.


The following shows possible values. Note that only a subset of the PROPVARIANT types supported by the built-in providers can be used as a property constraint. 



<p class="indent">VT_BOOL

<p class="indent">VT_I2

<p class="indent">VT_I4

<p class="indent">VT_I8

<p class="indent">VT_INT

<p class="indent">VT_LPWSTR

<p class="indent">VT_LPWSTR|VT_VECTOR

<p class="indent">VT_UI2

<p class="indent">VT_UI4

<p class="indent">VT_UI8

<p class="indent">VT_UINT


### -param enumPropertyConstraint [in]

A <a href="https://msdn.microsoft.com/59a3d957-0720-4bd9-b240-512b9cca3c90">PropertyConstraint</a> value that specifies the type of comparison to use when comparing the constraint's PKEY to the function instance's PKEY.


## -returns



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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The constraint specified for the query is not supported.  Either the constraint is not supported for a specific <b>VARENUM</b> type, or the <b>VARENUM</b> type is not supported at all. 

</td>
</tr>
</table>
 




## -remarks



A function instance will only match a property constraint when the PROPVARIANT type of the function instance's PKEY matches the PROPVARIANT type of the constraint's  PKEY and the function instance's PKEY value matches the constraint's PKEY value using the comparison operator specified by <i>enumPropertyConstraint</i>.

If multiple constraints are added, all constraints must be supported to satisfy the query.




## -see-also




<a href="https://msdn.microsoft.com/3c255fb4-8f9d-47a2-9770-1aa528d07f43">Function Discovery Queries</a>



<a href="https://msdn.microsoft.com/ae279ac1-ed7a-431b-a5aa-d60f5f9a64b0">IFunctionInstanceCollectionQuery</a>
 

 

