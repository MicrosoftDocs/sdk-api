---
UID: NF:netfw.INetFwOpenPort.put_Protocol
title: INetFwOpenPort::put_Protocol (netfw.h)
description: Specifies the protocol type setting for this port. (Put)
helpviewer_keywords: ["INetFwOpenPort interface [ICS/ICF]","Protocol property","INetFwOpenPort.Protocol","INetFwOpenPort.put_Protocol","INetFwOpenPort::Protocol","INetFwOpenPort::get_Protocol","INetFwOpenPort::put_Protocol","Protocol property [ICS/ICF]","Protocol property [ICS/ICF]","INetFwOpenPort interface","ics.inetfwopenport_protocol","netfw/INetFwOpenPort::Protocol","netfw/INetFwOpenPort::get_Protocol","netfw/INetFwOpenPort::put_Protocol","put_Protocol"]
old-location: ics\inetfwopenport_protocol.htm
tech.root: ics
ms.assetid: 775c3d29-89c7-4768-9476-2e56555fd82b
ms.date: 12/05/2018
ms.keywords: INetFwOpenPort interface [ICS/ICF],Protocol property, INetFwOpenPort.Protocol, INetFwOpenPort.put_Protocol, INetFwOpenPort::Protocol, INetFwOpenPort::get_Protocol, INetFwOpenPort::put_Protocol, Protocol property [ICS/ICF], Protocol property [ICS/ICF],INetFwOpenPort interface, ics.inetfwopenport_protocol, netfw/INetFwOpenPort::Protocol, netfw/INetFwOpenPort::get_Protocol, netfw/INetFwOpenPort::put_Protocol, put_Protocol
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwOpenPort::put_Protocol
 - netfw/INetFwOpenPort::put_Protocol
dev_langs:
 - c++
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
---

# INetFwOpenPort::put_Protocol


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies the protocol type setting  for this port.

This property is read/write.

## -parameters

## -remarks

The default protocol type is TCP for new ports.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenport">INetFwOpenPort</a>



<a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_ip_protocol">NET_FW_IP_PROTOCOL</a>
