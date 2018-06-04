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

# IFunctionInstanceCollectionQuery::AddQueryConstraint


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>AddQueryConstraint</b> method  adds a query constraint to the query.

This method enables the application to filter the result set to only those instances that fulfill this constraint.


## -parameters




### -param pszConstraintName [in]

The query constraint.


### -param pszConstraintValue [in]

The constraint value.


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
</table>
 




## -remarks



If multiple constraints are added, all constraints must be supported to satisfy the query.

<b>AddQueryConstraint</b> will fail with an error if the  <a href="https://msdn.microsoft.com/ae279ac1-ed7a-431b-a5aa-d60f5f9a64b0">IFunctionInstanceCollectionQuery</a> object includes all subcategories and the <b>AddQueryConstraint</b> method is called with the  <i>pszConstraintName</i> parameter set to <b>FD_QUERYCONSTRAINT_PROVIDERINSTANCEID</b>. To avoid this error, create a <b>IFunctionInstanceCollectionQuery</b> object that does not include all subcategories. You can create such an object by calling <a href="https://msdn.microsoft.com/46f74e55-8060-4f02-85e3-dbd2fc8fce78">CreateInstanceCollectionQuery</a> with the <i>fIncludeAllSubCategories</i> parameter set to <b>false</b>.




## -see-also




<a href="https://msdn.microsoft.com/13502fbd-bc88-4c28-939e-3e964ab6bb5d">Constraint Definitions</a>



<a href="https://msdn.microsoft.com/3c255fb4-8f9d-47a2-9770-1aa528d07f43">Function Discovery Queries</a>



<a href="https://msdn.microsoft.com/ae279ac1-ed7a-431b-a5aa-d60f5f9a64b0">IFunctionInstanceCollectionQuery</a>
 

 

