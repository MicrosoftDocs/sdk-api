---
UID: NF:netfw.INetFwRule.get_RemotePorts
title: INetFwRule::get_RemotePorts (netfw.h)
description: Specifies the list of remote ports for this rule. (Get)
helpviewer_keywords: ["INetFwRule interface [ICS/ICF]","RemotePorts property","INetFwRule.RemotePorts","INetFwRule.get_RemotePorts","INetFwRule::RemotePorts","INetFwRule::get_RemotePorts","INetFwRule::put_RemotePorts","RemotePorts property [ICS/ICF]","RemotePorts property [ICS/ICF]","INetFwRule interface","get_RemotePorts","ics.inetfwrule_remoteports","netfw/INetFwRule::RemotePorts","netfw/INetFwRule::get_RemotePorts","netfw/INetFwRule::put_RemotePorts"]
old-location: ics\inetfwrule_remoteports.htm
tech.root: ics
ms.assetid: e6791258-4669-42d9-9551-5c861bfb2b52
ms.date: 12/05/2018
ms.keywords: INetFwRule interface [ICS/ICF],RemotePorts property, INetFwRule.RemotePorts, INetFwRule.get_RemotePorts, INetFwRule::RemotePorts, INetFwRule::get_RemotePorts, INetFwRule::put_RemotePorts, RemotePorts property [ICS/ICF], RemotePorts property [ICS/ICF],INetFwRule interface, get_RemotePorts, ics.inetfwrule_remoteports, netfw/INetFwRule::RemotePorts, netfw/INetFwRule::get_RemotePorts, netfw/INetFwRule::put_RemotePorts
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
 - INetFwRule::get_RemotePorts
 - netfw/INetFwRule::get_RemotePorts
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
 - INetFwRule.RemotePorts
 - INetFwRule.get_RemotePorts
 - INetFwRule.put_RemotePorts
---

# INetFwRule::get_RemotePorts


## -description

Specifies the list of remote ports for this rule.

This property is read/write.

## -parameters

## -remarks

This property is optional.

Also see the restrictions on changing properties described in the Remarks section of the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> interface page.

The <a href="/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_protocol">Protocol</a> property must be set before the <b>RemotePorts</b> property or an error will be returned.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a>
