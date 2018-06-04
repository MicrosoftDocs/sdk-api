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

# _ENUM_SERVICE_STATUSA structure


## -description


Contains the name of a service in a service control manager database and information about that service. It is used by the 
<a href="https://msdn.microsoft.com/905d4453-96d4-4055-8a17-36714c547cdd">EnumDependentServices</a> and 
<a href="https://msdn.microsoft.com/3a82ac0e-f3e8-4a5a-9b13-84e952712229">EnumServicesStatus</a> functions.


## -struct-fields




### -field lpServiceName

The name of a service in the service control manager database. The maximum string length is 256 characters. The service control manager database preserves the case of the characters, but service name comparisons are always case insensitive. A slash (/), backslash (\), comma, and space are invalid service name characters.


### -field lpDisplayName

A display name that can be used by service control programs, such as Services in Control Panel, to identify the service. This string has a maximum length of 256 characters. The name is case-preserved in the service control manager. Display name comparisons are always case-insensitive.


### -field ServiceStatus

A 
<a href="https://msdn.microsoft.com/d268609b-d442-4d0f-9d49-ed23fee84961">SERVICE_STATUS</a> structure that contains status information for the <b>lpServiceName</b> service.


## -see-also




<a href="https://msdn.microsoft.com/905d4453-96d4-4055-8a17-36714c547cdd">EnumDependentServices</a>



<a href="https://msdn.microsoft.com/3a82ac0e-f3e8-4a5a-9b13-84e952712229">EnumServicesStatus</a>



<a href="https://msdn.microsoft.com/d268609b-d442-4d0f-9d49-ed23fee84961">SERVICE_STATUS</a>
 

 

