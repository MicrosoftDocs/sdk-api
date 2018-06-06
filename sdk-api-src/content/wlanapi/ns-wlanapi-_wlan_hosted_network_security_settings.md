---
UID: NS:wlanapi._WLAN_HOSTED_NETWORK_SECURITY_SETTINGS
title: "_WLAN_HOSTED_NETWORK_SECURITY_SETTINGS"
author: windows-sdk-content
description: Contains information about the security settings on the wireless Hosted Network.
old-location: nwifi\wlan_hosted_network_security_settings.htm
old-project: NativeWiFi
ms.assetid: b86beb10-52e5-4bc0-95fe-08307f8d1ccd
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: "*PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS, PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS, PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS structure pointer [NativeWIFI], WLAN_HOSTED_NETWORK_SECURITY_SETTINGS, WLAN_HOSTED_NETWORK_SECURITY_SETTINGS structure [NativeWIFI], _WLAN_HOSTED_NETWORK_SECURITY_SETTINGS, nwifi.wlan_hosted_network_security_settings, wlanapi/PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS, wlanapi/WLAN_HOSTED_NETWORK_SECURITY_SETTINGS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WLAN_HOSTED_NETWORK_SECURITY_SETTINGS, *PWLAN_HOSTED_NETWORK_SECURITY_SETTINGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wlanapi.h
api_name:
 - WLAN_HOSTED_NETWORK_SECURITY_SETTINGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WLAN_HOSTED_NETWORK_SECURITY_SETTINGS structure


## -description


The <b>WLAN_HOSTED_NETWORK_SECURITY_SETTINGS</b> structure contains information about the security settings on the wireless Hosted Network.


## -struct-fields




### -field dot11AuthAlgo

The authentication algorithm used by the wireless Hosted Network.


### -field dot11CipherAlgo

The cipher algorithm used by the wireless Hosted Network.


## -remarks



The <b>WLAN_HOSTED_NETWORK_SECURITY_SETTINGS</b>  structure is an extension to native wireless APIs added to support the wireless Hosted Network on Windows 7 and  later.  




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff547655">DOT11_AUTH_ALGORITHM</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547672">DOT11_CIPHER_ALGORITHM</a>



<a href="https://msdn.microsoft.com/bab05629-c921-4639-94db-25f77742dbd3">WlanHostedNetworkQueryProperty</a>
 

 

