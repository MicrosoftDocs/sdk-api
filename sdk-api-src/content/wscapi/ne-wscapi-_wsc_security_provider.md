---
UID: NE:wscapi._WSC_SECURITY_PROVIDER
title: "_WSC_SECURITY_PROVIDER"
author: windows-sdk-content
description: Defines all the services that are monitored by Windows Security Center (WSC).
old-location: winprog\wsc_security_provider.htm
old-project: devnotes
ms.assetid: b32664f4-9a1d-4fd2-ab2b-e3c5a8ddf187
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PWSC_SECURITY_PROVIDER, WSC_SECURITY_PROVIDER, WSC_SECURITY_PROVIDER enumeration [Windows API], WSC_SECURITY_PROVIDER,*PWSC_SECURITY_PROVIDER, WSC_SECURITY_PROVIDER,*PWSC_SECURITY_PROVIDER enumeration [Windows API], WSC_SECURITY_PROVIDER_ALL, WSC_SECURITY_PROVIDER_ANTISPYWARE, WSC_SECURITY_PROVIDER_ANTIVIRUS, WSC_SECURITY_PROVIDER_AUTOUPDATE_SETTINGS, WSC_SECURITY_PROVIDER_FIREWALL, WSC_SECURITY_PROVIDER_INTERNET_SETTINGS, WSC_SECURITY_PROVIDER_NONE, WSC_SECURITY_PROVIDER_SERVICE, WSC_SECURITY_PROVIDER_USER_ACCOUNT_CONTROL, _WSC_SECURITY_PROVIDER, winprog.wsc_security_provider, wscapi/WSC_SECURITY_PROVIDER, wscapi/WSC_SECURITY_PROVIDER_ALL, wscapi/WSC_SECURITY_PROVIDER_ANTISPYWARE, wscapi/WSC_SECURITY_PROVIDER_ANTIVIRUS, wscapi/WSC_SECURITY_PROVIDER_AUTOUPDATE_SETTINGS, wscapi/WSC_SECURITY_PROVIDER_FIREWALL, wscapi/WSC_SECURITY_PROVIDER_INTERNET_SETTINGS, wscapi/WSC_SECURITY_PROVIDER_NONE, wscapi/WSC_SECURITY_PROVIDER_SERVICE, wscapi/WSC_SECURITY_PROVIDER_USER_ACCOUNT_CONTROL"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wscapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSC_SECURITY_PROVIDER, *PWSC_SECURITY_PROVIDER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wscapi.h
api_name:
 - WSC_SECURITY_PROVIDER, *PWSC_SECURITY_PROVIDER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

