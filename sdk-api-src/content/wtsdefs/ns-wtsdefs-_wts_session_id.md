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

# _WTS_SESSION_ID structure


## -description


Contains a <b>GUID</b> that uniquely identifies a session.


## -struct-fields




### -field SessionUniqueGuid

A GUID that specifies the client connection.


### -field SessionId

An integer that specifies the session associated with the client connection.


## -remarks



This structure is used in the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/541bf463-9a4a-4237-8a61-1288ab1540cc">AuthenticateClientToSession</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6065e827-23a5-4150-bda5-999b7acede65">LogonNotify</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5a545f66-7143-419d-9e0c-a96070472ce5">NotifySessionId</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/541bf463-9a4a-4237-8a61-1288ab1540cc">AuthenticateClientToSession</a>



<a href="https://msdn.microsoft.com/6065e827-23a5-4150-bda5-999b7acede65">LogonNotify</a>



<a href="https://msdn.microsoft.com/5a545f66-7143-419d-9e0c-a96070472ce5">NotifySessionId</a>



<a href="https://msdn.microsoft.com/45d17758-4554-42aa-aeb9-c8d4e7fc6bb7">Remote Desktop Protocol Provider Structures</a>
 

 

