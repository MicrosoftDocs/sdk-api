---
UID: NF:netfw.INetFwOpenPort.get_Protocol
title: INetFwOpenPort::get_Protocol
author: windows-sdk-content
description: Specifies the protocol type setting for this port.
old-location: ics\inetfwopenport_protocol.htm
tech.root: ics
ms.assetid: 775c3d29-89c7-4768-9476-2e56555fd82b
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: INetFwOpenPort interface [ICS/ICF],Protocol property, INetFwOpenPort.Protocol, INetFwOpenPort.get_Protocol, INetFwOpenPort::Protocol, INetFwOpenPort::get_Protocol, INetFwOpenPort::put_Protocol, Protocol property [ICS/ICF], Protocol property [ICS/ICF],INetFwOpenPort interface, get_Protocol, ics.inetfwopenport_protocol, netfw/INetFwOpenPort::Protocol, netfw/INetFwOpenPort::get_Protocol, netfw/INetFwOpenPort::put_Protocol
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
 - INetFwOpenPort.Protocol
 - INetFwOpenPort.get_Protocol
 - INetFwOpenPort.put_Protocol
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwOpenPort::get_Protocol


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies the protocol type setting  for this port.

This property is read/write.


## -parameters


## -remarks



The default protocol type is TCP for new ports.




## -see-also




<a href="https://msdn.microsoft.com/1a9fd676-b1c0-4be5-9571-d14ac5980af5">INetFwOpenPort</a>



<a href="https://msdn.microsoft.com/867a038c-ae8e-4da8-a3e9-3ca7cb6ba518">NET_FW_IP_PROTOCOL</a>
 

 

