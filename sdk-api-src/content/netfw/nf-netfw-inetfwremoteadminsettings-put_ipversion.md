---
UID: NF:netfw.INetFwRemoteAdminSettings.put_IpVersion
title: INetFwRemoteAdminSettings::put_IpVersion
author: windows-driver-content
description: Specifies the IP version.
old-location: ics\inetfwremoteadminsettings_ipversion.htm
old-project: ICS
ms.assetid: 55303549-84d7-42d1-b722-a281acd50648
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: INetFwRemoteAdminSettings interface [ICS/ICF],IpVersion property, INetFwRemoteAdminSettings.IpVersion, INetFwRemoteAdminSettings.put_IpVersion, INetFwRemoteAdminSettings::IpVersion, INetFwRemoteAdminSettings::get_IpVersion, INetFwRemoteAdminSettings::put_IpVersion, IpVersion property [ICS/ICF], IpVersion property [ICS/ICF],INetFwRemoteAdminSettings interface, ics.inetfwremoteadminsettings_ipversion, netfw/INetFwRemoteAdminSettings::IpVersion, netfw/INetFwRemoteAdminSettings::get_IpVersion, netfw/INetFwRemoteAdminSettings::put_IpVersion, put_IpVersion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NETISO_ERROR_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FirewallAPI.dll
-	Hnetcfg.dll
api_name:
-	INetFwRemoteAdminSettings.IpVersion
-	INetFwRemoteAdminSettings.get_IpVersion
-	INetFwRemoteAdminSettings.put_IpVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetFwRemoteAdminSettings::put_IpVersion


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies the IP version.

This property is read/write.


## -parameters


## -remarks



This is the IP version for which remote admin is authorized. 

Only
    <b>NET_FW_IP_VERSION_ANY</b> is supported.




## -see-also




<a href="https://msdn.microsoft.com/35f34a53-e73b-48be-ac79-9b7ab825c6ad">INetFwRemoteAdminSettings</a>



<a href="https://msdn.microsoft.com/f322c914-e84f-4c13-8200-06e5fe2bdab7">NET_FW_IP_VERSION</a>
 

 

