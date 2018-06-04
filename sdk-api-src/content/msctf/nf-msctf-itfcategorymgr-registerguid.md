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

# ITfCategoryMgr::RegisterGUID


## -description




## -parameters




### -param rguid [in]

Contains the GUID to obtain the identifier for.


### -param pguidatom [out]

Pointer to a <a href="https://msdn.microsoft.com/91696612-1829-4052-81d1-eddc23278d35">TfGuidAtom</a> value that receives the identifier of the GUID.


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
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pguidatom</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



Identical <b>GUID</b> values receive identical <b>TfGuidAtom</b> values.

A <b>TfGuidAtom</b> value is only valid within the process that <b>ITfCategoryMgr::RegisterGUID</b> is called from.




## -see-also




<a href="https://msdn.microsoft.com/26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4">
        ITfCategoryMgr
      </a>



<a href="https://msdn.microsoft.com/a5f5a67c-3152-4933-8a35-0a0cd555a0bf">
        ITfCategoryMgr::GetGUID
      </a>



<a href="https://msdn.microsoft.com/813916f6-610f-4031-bb17-67d7f5ffed6f">
        ITfCategoryMgr::IsEqualTfGuidAtom
      </a>



<a href="https://msdn.microsoft.com/91696612-1829-4052-81d1-eddc23278d35">TfGuidAtom
      </a>
 

 

