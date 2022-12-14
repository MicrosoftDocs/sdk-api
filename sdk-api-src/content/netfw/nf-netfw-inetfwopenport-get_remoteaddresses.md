---
UID: NF:netfw.INetFwOpenPort.get_RemoteAddresses
title: INetFwOpenPort::get_RemoteAddresses (netfw.h)
description: Specifies a set of remote addresses from which the port can listen for traffic. (Get)
helpviewer_keywords: ["INetFwOpenPort interface [ICS/ICF]","RemoteAddresses property","INetFwOpenPort.RemoteAddresses","INetFwOpenPort.get_RemoteAddresses","INetFwOpenPort::RemoteAddresses","INetFwOpenPort::get_RemoteAddresses","INetFwOpenPort::put_RemoteAddresses","RemoteAddresses property [ICS/ICF]","RemoteAddresses property [ICS/ICF]","INetFwOpenPort interface","get_RemoteAddresses","ics.inetfwopenport_remoteaddresses","netfw/INetFwOpenPort::RemoteAddresses","netfw/INetFwOpenPort::get_RemoteAddresses","netfw/INetFwOpenPort::put_RemoteAddresses"]
old-location: ics\inetfwopenport_remoteaddresses.htm
tech.root: ics
ms.assetid: 5c38a9fc-b7d9-436d-92e6-8b0aec5e8628
ms.date: 12/05/2018
ms.keywords: INetFwOpenPort interface [ICS/ICF],RemoteAddresses property, INetFwOpenPort.RemoteAddresses, INetFwOpenPort.get_RemoteAddresses, INetFwOpenPort::RemoteAddresses, INetFwOpenPort::get_RemoteAddresses, INetFwOpenPort::put_RemoteAddresses, RemoteAddresses property [ICS/ICF], RemoteAddresses property [ICS/ICF],INetFwOpenPort interface, get_RemoteAddresses, ics.inetfwopenport_remoteaddresses, netfw/INetFwOpenPort::RemoteAddresses, netfw/INetFwOpenPort::get_RemoteAddresses, netfw/INetFwOpenPort::put_RemoteAddresses
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
 - INetFwOpenPort::get_RemoteAddresses
 - netfw/INetFwOpenPort::get_RemoteAddresses
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
 - INetFwOpenPort.RemoteAddresses
 - INetFwOpenPort.get_RemoteAddresses
 - INetFwOpenPort.put_RemoteAddresses
---

# INetFwOpenPort::get_RemoteAddresses


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies a set of remote addresses from which the port can listen for
   traffic.

This property is read/write.

## -parameters

## -remarks

The <i>remoteAddrs</i> parameter consists of one or more comma-delimited tokens specifying the remote addresses from which the application can listen for traffic. The default value is "*". 

Valid tokens:


<ul>
<li>"*": any remote address; if present, it must be the only token.</li>
<li>"LocalSubnet": not case-sensitive; specifying more than once has no effect.</li>
<li>subnet: may be specified using either subnet mask or network prefix notation. If neither a subnet mask nor a network prefix is specified, the subnet mask defaults to 255.255.255.255. Examples of valid subnets: 
10.0.0.2/255.0.0.0 
10.0.0.2/8 
10.0.0.2</li>
<li>Windows Vista: A valid IPv6 address.</li>
<li>Windows Vista: An IPv4 address range in the format "start address - end address."</li>
<li>Windows Vista: An IPv6 address range in the format "start address - end address."</li>
</ul>
For a predefined address range, use the <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_scope">Scope</a> property.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenport">INetFwOpenPort</a>
