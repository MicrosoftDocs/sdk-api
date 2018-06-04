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

# IViewObject::Unfreeze


## -description


Releases a drawing that was previously frozen using <a href="https://msdn.microsoft.com/943faf31-7de4-45da-887b-7ded479ac732">IViewObject::Freeze</a>. The most common use of this method is for banded printing.


## -parameters




### -param dwFreeze [in]

Contains a key previously returned from <a href="https://msdn.microsoft.com/943faf31-7de4-45da-887b-7ded479ac732">IViewObject::Freeze</a> that determines which view object to unfreeze.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
Error in the unfreezing process or the object is currently not frozen.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4310c987-3542-4a59-a6fb-951143001741">IViewObject</a>



<a href="https://msdn.microsoft.com/943faf31-7de4-45da-887b-7ded479ac732">IViewObject::Freeze</a>
 

 

