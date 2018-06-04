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

# IEnhancedStorageSiloAction::GetName


## -description


Returns a string for the name of the action specified by the <a href="https://msdn.microsoft.com/6deb7e22-f153-45fd-98ea-53a2e5692df7">IEnhancedStorageSiloAction</a> object.


## -parameters




### -param ppwszActionName [out]

Pointer to a string that represents the silo action by name.


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
The  action name was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppwszActionName</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



A name string is short, consisting of one or two words, and is suitable for display in a UI element such as a menu item or button label.

When the caller no longer requires access to the string, this buffer must be freed by passing this pointer to <a href="http://go.microsoft.com/fwlink/p/?linkid=134839">CoTaskMemFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/6deb7e22-f153-45fd-98ea-53a2e5692df7">IEnhancedStorageSiloAction</a>
 

 

