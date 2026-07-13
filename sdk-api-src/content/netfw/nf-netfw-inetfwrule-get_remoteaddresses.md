---
UID: NF:netfw.INetFwRule.get_RemoteAddresses
title: INetFwRule::get_RemoteAddresses (netfw.h)
description: Specifies the list of remote addresses for this rule. (Get)
helpviewer_keywords: ["INetFwRule interface [ICS/ICF]","RemoteAddresses property","INetFwRule.RemoteAddresses","INetFwRule.get_RemoteAddresses","INetFwRule::RemoteAddresses","INetFwRule::get_RemoteAddresses","INetFwRule::put_RemoteAddresses","RemoteAddresses property [ICS/ICF]","RemoteAddresses property [ICS/ICF]","INetFwRule interface","get_RemoteAddresses","ics.inetfwrule_remoteaddresses","netfw/INetFwRule::RemoteAddresses","netfw/INetFwRule::get_RemoteAddresses","netfw/INetFwRule::put_RemoteAddresses"]
old-location: ics\inetfwrule_remoteaddresses.htm
tech.root: ics
ms.assetid: 107e8cad-a603-4ac8-aa3c-6a85d47016ef
ms.date: 12/05/2018
ms.keywords: INetFwRule interface [ICS/ICF],RemoteAddresses property, INetFwRule.RemoteAddresses, INetFwRule.get_RemoteAddresses, INetFwRule::RemoteAddresses, INetFwRule::get_RemoteAddresses, INetFwRule::put_RemoteAddresses, RemoteAddresses property [ICS/ICF], RemoteAddresses property [ICS/ICF],INetFwRule interface, get_RemoteAddresses, ics.inetfwrule_remoteaddresses, netfw/INetFwRule::RemoteAddresses, netfw/INetFwRule::get_RemoteAddresses, netfw/INetFwRule::put_RemoteAddresses
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: FirewallAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwRule::get_RemoteAddresses
 - netfw/INetFwRule::get_RemoteAddresses
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwRule.RemoteAddresses
 - INetFwRule.get_RemoteAddresses
 - INetFwRule.put_RemoteAddresses
---

# INetFwRule::get_RemoteAddresses


## -description

Specifies  the list of remote addresses for this rule.

This property is read/write.

## -parameters

## -remarks

This property is optional.

Also see the restrictions on changing properties described in the Remarks section of the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> interface page.

The <i>remoteAddrs</i> parameter consists of one or more comma-delimited tokens specifying the remote addresses from which the application can listen for traffic.  The default value is "*". Valid tokens include:

<ul>
<li>"*" indicates any remote address.  If present, this must be the only token included.</li>
<li>"Defaultgateway"</li>
<li>"DHCP"</li>
<li>"DNS"</li>
<li>"WINS"</li>
<li>"LocalSubnet" indicates any local address on the local subnet.  This token is not case-sensitive.</li>
<li>A subnet can be specified using either the subnet mask or network prefix notation.  If neither a subnet mask not a network prefix is specified, the subnet mask defaults to 255.255.255.255.</li>
<li>A valid IPv6 address.</li>
<li>An IPv4 address range in the format of "start address - end address" with no spaces included.</li>
<li>An IPv6 address range in the format of "start address - end address" with no spaces included.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a>
