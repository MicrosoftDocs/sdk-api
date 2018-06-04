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

# IContactManager::MergeContactIDs


## -description


Makes an old Contact ID resolve to the same value as a new Contact ID. 
		Subsequent calls to <a href="https://msdn.microsoft.com/d9addc49-72fd-4b87-bf48-a2a09b1161e9">IContactManager::Load</a> with the old contact ID 
		now loads the new contact ID contact.


## -parameters




### -param pszNewContactID [in]

Type: <b>LPWSTR</b>

Specifies the ID of the new contact, representing both the old and new contacts.


### -param pszOldContactID [in]

Type: <b>LPCWSTR</b>

Specifies the ID representing the old contact. 


## -returns



Type: <b>HRESULT</b>

Returns one of the following values:

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
Address change was successful. 

</td>
</tr>
</table>
 



