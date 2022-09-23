---
UID: NF:netfw.INetFwRule.put_Protocol
title: INetFwRule::put_Protocol (netfw.h)
description: Specifies the IP protocol of this rule. (Put)
helpviewer_keywords: ["INetFwRule interface [ICS/ICF]","Protocol property","INetFwRule.Protocol","INetFwRule.put_Protocol","INetFwRule::Protocol","INetFwRule::get_Protocol","INetFwRule::put_Protocol","Protocol property [ICS/ICF]","Protocol property [ICS/ICF]","INetFwRule interface","ics.inetfwrule_protocol","netfw/INetFwRule::Protocol","netfw/INetFwRule::get_Protocol","netfw/INetFwRule::put_Protocol","put_Protocol"]
old-location: ics\inetfwrule_protocol.htm
tech.root: ics
ms.assetid: 16f61a1d-770a-4be9-a43d-10ff9fe276fb
ms.date: 12/05/2018
ms.keywords: INetFwRule interface [ICS/ICF],Protocol property, INetFwRule.Protocol, INetFwRule.put_Protocol, INetFwRule::Protocol, INetFwRule::get_Protocol, INetFwRule::put_Protocol, Protocol property [ICS/ICF], Protocol property [ICS/ICF],INetFwRule interface, ics.inetfwrule_protocol, netfw/INetFwRule::Protocol, netfw/INetFwRule::get_Protocol, netfw/INetFwRule::put_Protocol, put_Protocol
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
 - INetFwRule::put_Protocol
 - netfw/INetFwRule::put_Protocol
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
 - INetFwRule.Protocol
 - INetFwRule.get_Protocol
 - INetFwRule.put_Protocol
---

# INetFwRule::put_Protocol


## -description

Specifies the IP protocol  of this rule.

This property is read/write.

## -parameters

## -remarks

This property is optional.

Also see the restrictions on changing properties described in the Remarks section of the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> interface page.

The <b>Protocol</b> property must be set before the <a href="/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_localports">LocalPorts</a> or <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_remoteports">RemotePorts</a> properties or an error will be returned.

A list of protocol numbers is available at the  <a href="https://www.iana.org/assignments/protocol-numbers/protocol-numbers.xml">IANA website</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a>
