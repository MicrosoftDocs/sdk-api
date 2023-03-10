---
UID: NF:netfw.INetFwRule.get_LocalPorts
title: INetFwRule::get_LocalPorts (netfw.h)
description: Specifies the list of local ports for this rule. (Get)
helpviewer_keywords: ["RPC","RPC-EPMap","Teredo","INetFwRule interface [ICS/ICF]","LocalPorts property","INetFwRule.LocalPorts","INetFwRule.get_LocalPorts","INetFwRule::LocalPorts","INetFwRule::get_LocalPorts","INetFwRule::put_LocalPorts","LocalPorts property [ICS/ICF]","LocalPorts property [ICS/ICF]","INetFwRule interface","get_LocalPorts","ics.inetfwrule_localports","netfw/INetFwRule::LocalPorts","netfw/INetFwRule::get_LocalPorts","netfw/INetFwRule::put_LocalPorts"]
old-location: ics\inetfwrule_localports.htm
tech.root: ics
ms.assetid: 72c4f00c-d5c4-4d93-892b-ec9a63f8df09
ms.date: 12/05/2018
ms.keywords: RPC, RPC-EPMap, Teredo, INetFwRule interface [ICS/ICF],LocalPorts property, INetFwRule.LocalPorts, INetFwRule.get_LocalPorts, INetFwRule::LocalPorts, INetFwRule::get_LocalPorts, INetFwRule::put_LocalPorts, LocalPorts property [ICS/ICF], LocalPorts property [ICS/ICF],INetFwRule interface, get_LocalPorts, ics.inetfwrule_localports, netfw/INetFwRule::LocalPorts, netfw/INetFwRule::get_LocalPorts, netfw/INetFwRule::put_LocalPorts
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
 - INetFwRule::get_LocalPorts
 - netfw/INetFwRule::get_LocalPorts
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
 - INetFwRule.LocalPorts
 - INetFwRule.get_LocalPorts
 - INetFwRule.put_LocalPorts
---

# INetFwRule::get_LocalPorts


## -description

Specifies the list of local ports for this rule.

This property is read/write.

## -parameters

## -remarks

This property is optional.

Also see the restrictions on changing properties described in the Remarks section of the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> interface page.

The <a href="/windows/desktop/api/netfw/nf-netfw-inetfwrule-get_protocol">Protocol</a> property must be set before the <b>LocalPorts</b> property or an error will be returned.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a>
