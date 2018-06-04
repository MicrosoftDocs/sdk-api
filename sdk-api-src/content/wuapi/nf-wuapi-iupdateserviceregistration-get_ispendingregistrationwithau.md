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

# IUpdateServiceRegistration::get_IsPendingRegistrationWithAU


## -description


Gets a Boolean value that indicates whether the service will also be registered with Automatic Updates, when added. The authorization cabinet file (.cab) of the service determines whether  the service can be added.

This property is read-only.


## -parameters


## -remarks



If the <a href="https://msdn.microsoft.com/798d1392-a8dc-4063-b33d-159a507161f1">RegistrationState</a> property is <b>usrsRegistrationPending</b>, registration with Automatic Updates is subject to the allowed settings that are specified in the authorization cabinet  file (.cab) for the service.  If the authorization cabinet file does not allow registration with Automatic Updates, the service will  be registered with Windows Update Agent (WUA). However, the service will  not be registered with Automatic Updates.




## -see-also




<a href="https://msdn.microsoft.com/729664f2-5f75-4e73-9ccc-150b2e201f66">IUpdateServiceRegistration</a>
 

 

