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

# ITfCategoryMgr::IsEqualTfGuidAtom


## -description




## -parameters




### -param guidatom [in]

Specifies an atom that represents a GUID in the internal table.


### -param rguid [in]

Specifies the address of the GUID to compare with the atom in the internal table.


### -param pfEqual [out]

Pointer to a Boolean variable that receives an indication of whether the atom represents the GUID.


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
The method was successful.

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
The specified <i>pfEqual</i> parameter was <b>NULL</b> on input.

</td>
</tr>
</table>
 




## -remarks



If the atom specified by the <i>guidatom</i> parameter represents the <b>GUID</b> specified by the <i>rguid</i> parameter, the <i>pfEqual</i> parameter receives a nonzero value. Otherwise, the <i>pfEqual</i> parameter receives zero.




## -see-also




<a href="https://msdn.microsoft.com/26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4">ITfCategoryMgr</a>



<a href="https://msdn.microsoft.com/a5f5a67c-3152-4933-8a35-0a0cd555a0bf">ITfCategoryMgr::GetGUID</a>



<a href="https://msdn.microsoft.com/d0de17d9-be3a-4f68-a77d-880047775952">ITfCategoryMgr::RegisterGUID</a>
 

 

