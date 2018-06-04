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

# _WSC_SECURITY_PROVIDER enumeration


## -description


Defines all the services that are monitored by Windows Security Center (WSC).


## -enum-fields




### -field WSC_SECURITY_PROVIDER_FIREWALL

The aggregation of all firewalls for this computer.


### -field WSC_SECURITY_PROVIDER_AUTOUPDATE_SETTINGS

The automatic update settings for this computer.


### -field WSC_SECURITY_PROVIDER_ANTIVIRUS

The aggregation of all antivirus products for this computer.


### -field WSC_SECURITY_PROVIDER_ANTISPYWARE

The aggregation of all anti-spyware products for this computer.


### -field WSC_SECURITY_PROVIDER_INTERNET_SETTINGS

The settings that restrict the access of web sites in each of the Internet zones for this computer.


### -field WSC_SECURITY_PROVIDER_USER_ACCOUNT_CONTROL

The User Account Control (UAC) settings for this computer.


### -field WSC_SECURITY_PROVIDER_SERVICE

The running state of the WSC service on this computer.


### -field WSC_SECURITY_PROVIDER_NONE

None of the items that WSC monitors.


### -field WSC_SECURITY_PROVIDER_ALL

All of the items that the WSC monitors.


## -see-also




<a href="https://msdn.microsoft.com/1193eba3-a01b-4ee3-a83d-25dcdbc15de0">WscGetSecurityProviderHealth</a>
 

 

