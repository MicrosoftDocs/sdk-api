---
UID: NF:netfw.INetFwOpenPort.put_IpVersion
title: INetFwOpenPort::put_IpVersion (netfw.h)
description: Specifies the IP version setting for this port. (Put)
helpviewer_keywords: ["INetFwOpenPort interface [ICS/ICF]","IpVersion property","INetFwOpenPort.IpVersion","INetFwOpenPort.put_IpVersion","INetFwOpenPort::IpVersion","INetFwOpenPort::get_IpVersion","INetFwOpenPort::put_IpVersion","IpVersion property [ICS/ICF]","IpVersion property [ICS/ICF]","INetFwOpenPort interface","ics.inetfwopenport_ipversion","netfw/INetFwOpenPort::IpVersion","netfw/INetFwOpenPort::get_IpVersion","netfw/INetFwOpenPort::put_IpVersion","put_IpVersion"]
old-location: ics\inetfwopenport_ipversion.htm
tech.root: ics
ms.assetid: fb5dfb78-fc0d-4dca-850a-683046b4e2a3
ms.date: 12/05/2018
ms.keywords: INetFwOpenPort interface [ICS/ICF],IpVersion property, INetFwOpenPort.IpVersion, INetFwOpenPort.put_IpVersion, INetFwOpenPort::IpVersion, INetFwOpenPort::get_IpVersion, INetFwOpenPort::put_IpVersion, IpVersion property [ICS/ICF], IpVersion property [ICS/ICF],INetFwOpenPort interface, ics.inetfwopenport_ipversion, netfw/INetFwOpenPort::IpVersion, netfw/INetFwOpenPort::get_IpVersion, netfw/INetFwOpenPort::put_IpVersion, put_IpVersion
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
 - INetFwOpenPort::put_IpVersion
 - netfw/INetFwOpenPort::put_IpVersion
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
 - INetFwOpenPort.IpVersion
 - INetFwOpenPort.get_IpVersion
 - INetFwOpenPort.put_IpVersion
---

# INetFwOpenPort::put_IpVersion


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies the IP version  setting for this port.

This property is read/write.

## -parameters

## -remarks

Only <b>NET_FW_IP_VERSION_ANY</b> is supported and this is the default for new ports.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenport">INetFwOpenPort</a>



<a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_ip_version">NET_FW_IP_VERSION</a>
