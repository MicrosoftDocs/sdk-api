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

# MI_Server_GetSystemName function


## -description


Gets the system name for the server.


## -parameters




### -param systemName

Returned system name.


## -returns



This function returns MI_Result MI_CALL.




## -remarks



This function is only available from within a generated provider. It obtains the system name for this server. The system name is used in several standard CIM key properties (for example, CIM_Fan.SystemName). The name is only known by the server. The provider should use only this function to get the system name and should never attempt to determine the system name using other means. The system name is typically the host name for the system, but the server may add additional qualification.



