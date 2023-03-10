---
UID: NF:netfw.INetFwService.put_RemoteAddresses
title: INetFwService::put_RemoteAddresses (netfw.h)
description: Specifies a set of the remote addresses from which the service ports can listen for traffic. (Put)
helpviewer_keywords: ["INetFwService interface [ICS/ICF]","RemoteAddresses property","INetFwService.RemoteAddresses","INetFwService.put_RemoteAddresses","INetFwService::RemoteAddresses","INetFwService::get_RemoteAddresses","INetFwService::put_RemoteAddresses","RemoteAddresses property [ICS/ICF]","RemoteAddresses property [ICS/ICF]","INetFwService interface","ics.inetfwservice_remoteaddresses","netfw/INetFwService::RemoteAddresses","netfw/INetFwService::get_RemoteAddresses","netfw/INetFwService::put_RemoteAddresses","put_RemoteAddresses"]
old-location: ics\inetfwservice_remoteaddresses.htm
tech.root: ics
ms.assetid: 6cb1dfa1-1e92-47a8-9a97-45443f487f6e
ms.date: 12/05/2018
ms.keywords: INetFwService interface [ICS/ICF],RemoteAddresses property, INetFwService.RemoteAddresses, INetFwService.put_RemoteAddresses, INetFwService::RemoteAddresses, INetFwService::get_RemoteAddresses, INetFwService::put_RemoteAddresses, RemoteAddresses property [ICS/ICF], RemoteAddresses property [ICS/ICF],INetFwService interface, ics.inetfwservice_remoteaddresses, netfw/INetFwService::RemoteAddresses, netfw/INetFwService::get_RemoteAddresses, netfw/INetFwService::put_RemoteAddresses, put_RemoteAddresses
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
 - INetFwService::put_RemoteAddresses
 - netfw/INetFwService::put_RemoteAddresses
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
 - INetFwService.RemoteAddresses
 - INetFwService.get_RemoteAddresses
 - INetFwService.put_RemoteAddresses
---

# INetFwService::put_RemoteAddresses


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies a set  of the remote addresses from which the service ports can listen for traffic. 

This property is read/write.

## -parameters

## -remarks

If
   the service has been customized, get returns the union of the remote
   addresses for all the service ports.

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
For a predefined address range, use the <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwservice-get_scope">Scope</a> property.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwservice">INetFwService</a>
