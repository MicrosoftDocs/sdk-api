---
UID: NF:netfw.INetFwService.put_IpVersion
title: INetFwService::put_IpVersion
author: windows-sdk-content
description: Specifies the firewall IP version for which the service is authorized.
old-location: ics\inetfwservice_ipversion.htm
old-project: ics
ms.assetid: 992f39f6-ffb7-40c0-9227-6e626f226313
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: INetFwService interface [ICS/ICF],IpVersion property, INetFwService.IpVersion, INetFwService.put_IpVersion, INetFwService::IpVersion, INetFwService::get_IpVersion, INetFwService::put_IpVersion, IpVersion property [ICS/ICF], IpVersion property [ICS/ICF],INetFwService interface, ics.inetfwservice_ipversion, netfw/INetFwService::IpVersion, netfw/INetFwService::get_IpVersion, netfw/INetFwService::put_IpVersion, put_IpVersion
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NETISO_ERROR_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwService.IpVersion
 - INetFwService.get_IpVersion
 - INetFwService.put_IpVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwService::put_IpVersion


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies the firewall IP version  for which  the service is authorized.

This property is read/write.


## -parameters


## -remarks



Only
   <b>NET_FW_IP_VERSION_ANY</b> is supported.




## -see-also




<a href="https://msdn.microsoft.com/57a777a4-03f5-416a-ae28-474d8794a759">INetFwService</a>



<a href="https://msdn.microsoft.com/f322c914-e84f-4c13-8200-06e5fe2bdab7">NET_FW_IP_VERSION</a>
 

 

