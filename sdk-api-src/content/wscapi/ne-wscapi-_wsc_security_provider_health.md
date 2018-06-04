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

# _WSC_SECURITY_PROVIDER_HEALTH enumeration


## -description


Defines the possible states for any service monitored by Windows Security Center (WSC).


## -enum-fields




### -field WSC_SECURITY_PROVIDER_HEALTH_GOOD

The status of the security provider category is good and does not need user attention.


### -field WSC_SECURITY_PROVIDER_HEALTH_NOTMONITORED

The status of the security provider category is not monitored by WSC.


### -field WSC_SECURITY_PROVIDER_HEALTH_POOR

The status of the security provider category is poor and the computer may be at risk.


### -field WSC_SECURITY_PROVIDER_HEALTH_SNOOZE

The security provider category is in snooze state. Snooze indicates that WSC is not actively protecting the computer.


## -see-also




<a href="https://msdn.microsoft.com/1193eba3-a01b-4ee3-a83d-25dcdbc15de0">WscGetSecurityProviderHealth</a>
 

 

