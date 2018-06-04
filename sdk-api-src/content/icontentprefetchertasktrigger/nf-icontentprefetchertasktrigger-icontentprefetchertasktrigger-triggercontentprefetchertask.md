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

# IContentPrefetcherTaskTrigger::TriggerContentPrefetcherTask


## -description


Triggers a content prefetch background task for the specified app package.


## -parameters




### -param packageFullName [in]

The package ID.


## -returns



Returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The provided package ID is not an installed package that has registered for the content prefetch background task, or the package ID is empty or null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The method call was not made at the required Medium Integrity Level (Medium IL).


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5DB67142-4B8F-4B88-A77F-B69F48E75839">IContentPrefetcherTaskTrigger</a>
 

 

