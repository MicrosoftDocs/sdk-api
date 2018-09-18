---
UID: NF:netfw.INetFwOpenPort.put_IpVersion
title: INetFwOpenPort::put_IpVersion
author: windows-sdk-content
description: Specifies the IP version setting for this port.
old-location: ics\inetfwopenport_ipversion.htm
tech.root: ics
ms.assetid: fb5dfb78-fc0d-4dca-850a-683046b4e2a3
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: INetFwOpenPort interface [ICS/ICF],IpVersion property, INetFwOpenPort.IpVersion, INetFwOpenPort.put_IpVersion, INetFwOpenPort::IpVersion, INetFwOpenPort::get_IpVersion, INetFwOpenPort::put_IpVersion, IpVersion property [ICS/ICF], IpVersion property [ICS/ICF],INetFwOpenPort interface, ics.inetfwopenport_ipversion, netfw/INetFwOpenPort::IpVersion, netfw/INetFwOpenPort::get_IpVersion, netfw/INetFwOpenPort::put_IpVersion, put_IpVersion
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
 - INetFwOpenPort.IpVersion
 - INetFwOpenPort.get_IpVersion
 - INetFwOpenPort.put_IpVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwOpenPort::put_IpVersion


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies the IP version  setting for this port.

This property is read/write.


## -parameters


## -remarks



Only <b>NET_FW_IP_VERSION_ANY</b> is supported and this is the default for new ports.




## -see-also




<a href="https://msdn.microsoft.com/1a9fd676-b1c0-4be5-9571-d14ac5980af5">INetFwOpenPort</a>



<a href="https://msdn.microsoft.com/f322c914-e84f-4c13-8200-06e5fe2bdab7">NET_FW_IP_VERSION</a>
 

 

