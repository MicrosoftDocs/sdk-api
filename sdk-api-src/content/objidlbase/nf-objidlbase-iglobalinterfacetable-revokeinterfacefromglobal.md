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

# IGlobalInterfaceTable::RevokeInterfaceFromGlobal


## -description


Revokes the registration of an interface in the global interface table.


## -parameters




### -param dwCookie [in]

Identifies the interface whose global registration is to be revoked.


## -returns



This method can return the following values.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



Call this method when an interface registered in the global interface table object no longer needs to be accessed by other apartments in the same process. This method can be called by any apartment in the process, including apartments other than the one that registered the interface in the global interface table.




## -see-also




<a href="https://msdn.microsoft.com/0c1feee7-e33b-4b5d-8e35-4de6895e3947">IGlobalInterfaceTable</a>
 

 

