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

# ITPluggableTerminalSuperclassRegistration::Add


## -description


The 
<b>Add</b> method adds a pluggable terminal superclass to the registry. If the superclass already exists, the method modifies the information for the superclass.


## -parameters






## -returns



This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Method failed.

</td>
</tr>
</table>
 




## -remarks



The 
<b>Add</b> method adds a new terminal superclass if the CLSID does not exist as an entry in the registry. The method modifies the information about a terminal superclass if the CLSID already exists in the registry.

If the CLSID for the terminal superclass was not set for terminal superclass, the 
<b>Add</b> method fails.




## -see-also




<a href="https://msdn.microsoft.com/fe87d55f-1e1c-4241-b8a3-b56d2000f3ca">Delete</a>



<a href="https://msdn.microsoft.com/76f5d213-d1fb-4437-af09-9d915db05dc6">ITPluggableTerminalSuperclassRegistration</a>
 

 

