---
UID: NF:netfw.INetFwAuthorizedApplication.get_IpVersion
title: INetFwAuthorizedApplication::get_IpVersion
author: windows-sdk-content
description: Specifies the IP version setting for this application.
old-location: ics\inetfwauthorizedapplication_ipversion.htm
tech.root: ics
ms.assetid: f0a4127f-4f81-4b71-a5c5-ba9e30927820
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: INetFwAuthorizedApplication interface [ICS/ICF],IpVersion property, INetFwAuthorizedApplication.IpVersion, INetFwAuthorizedApplication.get_IpVersion, INetFwAuthorizedApplication::IpVersion, INetFwAuthorizedApplication::get_IpVersion, INetFwAuthorizedApplication::put_IpVersion, IpVersion property [ICS/ICF], IpVersion property [ICS/ICF],INetFwAuthorizedApplication interface, get_IpVersion, ics.inetfwauthorizedapplication_ipversion, netfw/INetFwAuthorizedApplication::IpVersion, netfw/INetFwAuthorizedApplication::get_IpVersion, netfw/INetFwAuthorizedApplication::put_IpVersion
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
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwAuthorizedApplication.IpVersion
 - INetFwAuthorizedApplication.get_IpVersion
 - INetFwAuthorizedApplication.put_IpVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwAuthorizedApplication::get_IpVersion


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies the IP version  setting for this application.

This property is read/write.


## -parameters


## -remarks



Only <a href="https://msdn.microsoft.com/f322c914-e84f-4c13-8200-06e5fe2bdab7">NET_FW_IP_VERSION_ANY</a> is supported and this is the default for new applications.




## -see-also




<a href="https://msdn.microsoft.com/1ddeeab8-b81b-4d34-9ca6-103147fb3426">INetFwAuthorizedApplication</a>



<a href="https://msdn.microsoft.com/f322c914-e84f-4c13-8200-06e5fe2bdab7">NET_FW_IP_VERSION</a>
 

 

