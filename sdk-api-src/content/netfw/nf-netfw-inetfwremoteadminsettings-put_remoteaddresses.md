---
UID: NF:netfw.INetFwRemoteAdminSettings.put_RemoteAddresses
title: INetFwRemoteAdminSettings::put_RemoteAddresses (netfw.h)
description: Specifies a set of remote addresses from which remote administration is allowed.
helpviewer_keywords: ["INetFwRemoteAdminSettings interface [ICS/ICF]","RemoteAddresses property","INetFwRemoteAdminSettings.RemoteAddresses","INetFwRemoteAdminSettings.put_RemoteAddresses","INetFwRemoteAdminSettings::RemoteAddresses","INetFwRemoteAdminSettings::get_RemoteAddresses","INetFwRemoteAdminSettings::put_RemoteAddresses","RemoteAddresses property [ICS/ICF]","RemoteAddresses property [ICS/ICF]","INetFwRemoteAdminSettings interface","ics.inetfwremoteadminsettings_remoteaddresses","netfw/INetFwRemoteAdminSettings::RemoteAddresses","netfw/INetFwRemoteAdminSettings::get_RemoteAddresses","netfw/INetFwRemoteAdminSettings::put_RemoteAddresses","put_RemoteAddresses"]
old-location: ics\inetfwremoteadminsettings_remoteaddresses.htm
tech.root: ics
ms.assetid: 9166617b-3e61-4d83-bd2f-92682ea5df82
ms.date: 12/05/2018
ms.keywords: INetFwRemoteAdminSettings interface [ICS/ICF],RemoteAddresses property, INetFwRemoteAdminSettings.RemoteAddresses, INetFwRemoteAdminSettings.put_RemoteAddresses, INetFwRemoteAdminSettings::RemoteAddresses, INetFwRemoteAdminSettings::get_RemoteAddresses, INetFwRemoteAdminSettings::put_RemoteAddresses, RemoteAddresses property [ICS/ICF], RemoteAddresses property [ICS/ICF],INetFwRemoteAdminSettings interface, ics.inetfwremoteadminsettings_remoteaddresses, netfw/INetFwRemoteAdminSettings::RemoteAddresses, netfw/INetFwRemoteAdminSettings::get_RemoteAddresses, netfw/INetFwRemoteAdminSettings::put_RemoteAddresses, put_RemoteAddresses
f1_keywords:
- netfw/INetFwRemoteAdminSettings.RemoteAddresses
dev_langs:
- c++
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
- INetFwRemoteAdminSettings.RemoteAddresses
- INetFwRemoteAdminSettings.get_RemoteAddresses
- INetFwRemoteAdminSettings.put_RemoteAddresses
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INetFwRemoteAdminSettings::put_RemoteAddresses


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies a set of remote addresses from which remote administration is allowed.

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
For a predefined address range, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwremoteadminsettings-get_scope">Scope</a> property.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/netfw/nn-netfw-inetfwremoteadminsettings">INetFwRemoteAdminSettings</a>
 

 

