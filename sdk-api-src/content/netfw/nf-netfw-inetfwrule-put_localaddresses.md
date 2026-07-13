---
UID: NF:netfw.INetFwRule.put_LocalAddresses
title: INetFwRule::put_LocalAddresses (netfw.h)
description: Specifies the list of local addresses for this rule. (Put)
helpviewer_keywords: ["INetFwRule interface [ICS/ICF]","LocalAddresses property","INetFwRule.LocalAddresses","INetFwRule.put_LocalAddresses","INetFwRule::LocalAddresses","INetFwRule::get_LocalAddresses","INetFwRule::put_LocalAddresses","LocalAddresses property [ICS/ICF]","LocalAddresses property [ICS/ICF]","INetFwRule interface","ics.inetfwrule_localaddresses","netfw/INetFwRule::LocalAddresses","netfw/INetFwRule::get_LocalAddresses","netfw/INetFwRule::put_LocalAddresses","put_LocalAddresses"]
old-location: ics\inetfwrule_localaddresses.htm
tech.root: ics
ms.assetid: e95c6545-770b-430f-a1fc-32dcaac0eaa0
ms.date: 12/05/2018
ms.keywords: INetFwRule interface [ICS/ICF],LocalAddresses property, INetFwRule.LocalAddresses, INetFwRule.put_LocalAddresses, INetFwRule::LocalAddresses, INetFwRule::get_LocalAddresses, INetFwRule::put_LocalAddresses, LocalAddresses property [ICS/ICF], LocalAddresses property [ICS/ICF],INetFwRule interface, ics.inetfwrule_localaddresses, netfw/INetFwRule::LocalAddresses, netfw/INetFwRule::get_LocalAddresses, netfw/INetFwRule::put_LocalAddresses, put_LocalAddresses
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
 - INetFwRule::put_LocalAddresses
 - netfw/INetFwRule::put_LocalAddresses
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
 - INetFwRule.LocalAddresses
 - INetFwRule.get_LocalAddresses
 - INetFwRule.put_LocalAddresses
---

# INetFwRule::put_LocalAddresses


## -description

Specifies the list of local addresses for this  rule.

This property is read/write.

## -parameters

## -remarks

This property is optional.

Also see the restrictions on changing properties described in the Remarks section of the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> interface page.

The <i>localAddrs</i> parameter consists of one or more comma-delimited tokens specifying the local addresses from which the application can listen for traffic.  "*" is the default value. Valid tokens include:

<ul>
<li>"*" indicates any local address.  If present, this must be the only token included.</li>
<li>"Defaultgateway"</li>
<li>"DHCP"</li>
<li>"WINS"</li>
<li>"LocalSubnet" indicates any local address on the local subnet.  This token is not case-sensitive.</li>
<li>A subnet can be specified using either the subnet mask or network prefix notation.  If neither a subnet mask not a network prefix is specified, the subnet mask defaults to 255.255.255.255.</li>
<li>A valid IPv6 address.</li>
<li>An IPv4 address range in the format of "start address - end address" with no spaces included.</li>
<li>An IPv6 address range in the format of "start address - end address" with no spaces included.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a>
