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

# IRendezvousApplication::SetRendezvousSession


## -description


Passes <a href="https://msdn.microsoft.com/3e6dc5c7-2238-4ea8-a4fb-75e4b56d3cfd">IRendezvousSession</a> to the Windows Remote Assistance application. This method is used by the instant messaging application. 


## -parameters




### -param pRendezvousSession [in]

<a href="https://msdn.microsoft.com/3e6dc5c7-2238-4ea8-a4fb-75e4b56d3cfd">IRendezvousSession</a>

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
The <a href="https://msdn.microsoft.com/3e6dc5c7-2238-4ea8-a4fb-75e4b56d3cfd">IRendezvousSession</a> was passed to the Windows Remote Assistance application successfully. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The session object passed to the method is not valid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
A catastrophic error occurred while trying to pass the session to the Windows Remote Assistance application.

</td>
</tr>
</table>
 



