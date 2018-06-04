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

# IEntity::Base


## -description



            Retrieves the parent entity of this entity.
        


## -parameters




### -param pBaseEntity [out, retval]

Type: <b><a href="https://msdn.microsoft.com/856018d4-5e72-421e-9760-49f5d8d77e79">IEntity</a>**</b>


          Receives a pointer to the parent <a href="https://msdn.microsoft.com/856018d4-5e72-421e-9760-49f5d8d77e79">IEntity</a> object, or <b>NULL</b> if there is no parent entity.
        


## -returns



Type: <b>HRESULT</b>


            Returns one of the following, or an error value otherwise.
        

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
<i>pBaseEntity</i> successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The entity has no parent; <i>pBaseEntity</i> successfully set to <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Each entity derives from some other entity, except the entity named Entity, for which this method returns S_FALSE. The derived entity inherits all relationships from the base entity.



