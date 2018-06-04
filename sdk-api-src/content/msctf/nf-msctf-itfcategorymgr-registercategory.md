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

# ITfCategoryMgr::RegisterCategory


## -description




## -parameters




### -param rclsid [in]

Contains the CLSID of the text service that owns the item.


### -param rcatid [in]

Contains a GUID value that identifies the category to register the item under. This can be a user-defined category or one of the <a href="https://msdn.microsoft.com/04c0632d-ac64-4081-ba95-c11feb3f40dd">predefined category values</a>.


### -param rguid [in]

Contains a GUID value that identifies the item to register.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4">ITfCategoryMgr
      </a>



<a href="https://msdn.microsoft.com/73013bc1-4623-4e00-b87b-29ea3d728e9f">
        ITfCategoryMgr::UnregisterCategory
      </a>



<a href="https://msdn.microsoft.com/04c0632d-ac64-4081-ba95-c11feb3f40dd">
        Predefined Category Values
      </a>
 

 

