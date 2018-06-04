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

# IContextProperties::GetProperty


## -description


Retrieves a context object property.


## -parameters




### -param name [in]

The name of the context object property to be retrieved.

The following are IIS intrinsic properties.

<ul>
<li>Application</li>
<li>Request</li>
<li>Response</li>
<li>Server</li>
<li>Session</li>
</ul>
The following is the COMTI instrinsic property:

<ul>
<li>host-security-callback.cedar.microsoft.com</li>
</ul>

### -param pProperty [out]

A pointer to the property.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



To retrieve an IIS object, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> using the VT_DISPATCH member of the returned <b>VARIANT</b> for the interface to the IIS object (for example, IResponse for the Response object).






## -see-also




<a href="https://msdn.microsoft.com/95a5cfda-7587-496e-ba16-0dd2e8a4db32">IContextProperties</a>
 

 

