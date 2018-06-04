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

# ITfCategoryMgr::FindClosestCategory


## -description




## -parameters




### -param rguid [in]

Specifies the address of the GUID for which to find the closest category.


### -param pcatid [out]

Pointer to the <b>GUID</b> that receives the CATID for the closest category.


### -param ppcatidList [in]

Pointer to a pointer that specifies an array of CATIDs to search for the closest category.


### -param ulCount [in]

Specifies the number of elements in the array of the <i>ppcatidList</i> parameter.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method obtained the closest category from the list of categories, or the method was unable to obtain a category from the list and indicates this with a <i>pcatid</i> parameter pointer to GUID_NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to find a category for the specified GUID and signals this with a <i>pcatid</i> parameter pointer to GUID_NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method cannot access the internal table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified <i>pcatid</i> parameter was <b>NULL</b> on input, or the list of categories contained a <b>NULL</b> element when the <i>ulCount</i> parameter was nonzero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to perform the operation.

</td>
</tr>
</table>
 




## -remarks



The closest category to a <b>GUID</b> is chosen in one of two modes. In the first mode, the method receives a non-empty category list. It chooses the first matching <b>CATID</b> from that list or GUID_NULL if the list does not contain a category that contains the <b>GUID</b> . In the second mode, it receives an empty category list. It chooses the first category that contains the <b>GUID</b> or GUID_NULL if no category contains the <b>GUID</b> .




## -see-also




<a href="https://msdn.microsoft.com/26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4">ITfCategoryMgr</a>



<a href="https://msdn.microsoft.com/271e5fbe-54e2-47e3-97d4-cd4211b92080">ITfCategoryMgr::EnumCategoriesInItem</a>



<a href="https://msdn.microsoft.com/88b123d8-86aa-40ae-8777-1b33cfbb953a">ITfCategoryMgr::EnumItemsInCategory</a>



<a href="https://msdn.microsoft.com/9e9a72a8-ea9b-4438-992c-5a7db64f7d82">ITfCategoryMgr::RegisterCategory</a>
 

 

