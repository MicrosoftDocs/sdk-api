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

# IContactManager::Initialize


## -description


Initializes the contact manager with the unique application name and application version 
		being used to manipulate contacts.


## -parameters




### -param pszAppName [in]

Type: <b>LPWSTR</b>

Specifies the application name.


### -param pszAppVersion [in]

Type: <b>LPCWSTR</b>

Specifies the application version. 


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

<a href="https://msdn.microsoft.com/d0102659-488c-45db-931b-345013e21eed">IContactManager</a> is initialized. 

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  This method MUST be called before other <a href="https://msdn.microsoft.com/d0102659-488c-45db-931b-345013e21eed">IContactManager</a> methods.</div>
<div> </div>


