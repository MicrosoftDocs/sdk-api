---
UID: NF:netfw.INetFwPolicy2.get_BlockAllInboundTraffic
title: INetFwPolicy2::get_BlockAllInboundTraffic (netfw.h)
description: Indicates whether the firewall should not allow inbound traffic. (Get)
helpviewer_keywords: ["BlockAllInboundTraffic property [ICS/ICF]","BlockAllInboundTraffic property [ICS/ICF]","INetFwPolicy2 interface","INetFwPolicy2 interface [ICS/ICF]","BlockAllInboundTraffic property","INetFwPolicy2.BlockAllInboundTraffic","INetFwPolicy2.get_BlockAllInboundTraffic","INetFwPolicy2::BlockAllInboundTraffic","INetFwPolicy2::get_BlockAllInboundTraffic","INetFwPolicy2::put_BlockAllInboundTraffic","get_BlockAllInboundTraffic","ics.inetfwpolicy2_exceptionsnotallowed","netfw/INetFwPolicy2::BlockAllInboundTraffic","netfw/INetFwPolicy2::get_BlockAllInboundTraffic","netfw/INetFwPolicy2::put_BlockAllInboundTraffic"]
old-location: ics\inetfwpolicy2_exceptionsnotallowed.htm
tech.root: ics
ms.assetid: c40e58fd-b372-4d94-bcf1-bad1e84321f7
ms.date: 12/05/2018
ms.keywords: BlockAllInboundTraffic property [ICS/ICF], BlockAllInboundTraffic property [ICS/ICF],INetFwPolicy2 interface, INetFwPolicy2 interface [ICS/ICF],BlockAllInboundTraffic property, INetFwPolicy2.BlockAllInboundTraffic, INetFwPolicy2.get_BlockAllInboundTraffic, INetFwPolicy2::BlockAllInboundTraffic, INetFwPolicy2::get_BlockAllInboundTraffic, INetFwPolicy2::put_BlockAllInboundTraffic, get_BlockAllInboundTraffic, ics.inetfwpolicy2_exceptionsnotallowed, netfw/INetFwPolicy2::BlockAllInboundTraffic, netfw/INetFwPolicy2::get_BlockAllInboundTraffic, netfw/INetFwPolicy2::put_BlockAllInboundTraffic
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
 - INetFwPolicy2::get_BlockAllInboundTraffic
 - netfw/INetFwPolicy2::get_BlockAllInboundTraffic
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
 - INetFwPolicy2.BlockAllInboundTraffic
 - INetFwPolicy2.get_BlockAllInboundTraffic
 - INetFwPolicy2.put_BlockAllInboundTraffic
---

# INetFwPolicy2::get_BlockAllInboundTraffic


## -description

Indicates whether the firewall should not allow inbound traffic.

This property is read/write.

## -parameters

## -remarks

All interfaces are firewall-enabled. This means that all the exceptions (such as GloballyOpenPorts, Applications, or Services) which are  specified in the profile are ignored
   and only locally-initiated traffic is allowed.

When you pass a profile type obtained from the <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_currentprofiletypes">CurrentProfileTypes</a> property, make sure that you pass only one profile type to <b>get_BlockAllInboundTraffic</b> and <b>put_BlockAllInboundTraffic</b>. Note that <b>get_CurrentProfileTypes</b> can return multiple profiles.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2">INetFwPolicy2</a>
