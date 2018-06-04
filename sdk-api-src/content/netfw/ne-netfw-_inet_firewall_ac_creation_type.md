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

# _INET_FIREWALL_AC_CREATION_TYPE enumeration


## -description


The <b>INET_FIREWALL_AC_CREATION_TYPE</b> enumeration specifies the type of app container creation events for which notifications will be delivered.


## -enum-fields




### -field INET_FIREWALL_AC_NONE

This value is reserved for system use.


### -field INET_FIREWALL_AC_PACKAGE_ID_ONLY

Notifications will be delivered when an app container is created with a package identifier.


### -field INET_FIREWALL_AC_BINARY

Notifications will be delivered when an app container is created with a binary path.


### -field INET_FIREWALL_AC_MAX

Maximum value for testing purposes.


## -see-also




<a href="https://msdn.microsoft.com/b5f1b85d-3538-4be3-b97b-f9207cc7063b">INET_FIREWALL_AC_CHANGE</a>
 

 

