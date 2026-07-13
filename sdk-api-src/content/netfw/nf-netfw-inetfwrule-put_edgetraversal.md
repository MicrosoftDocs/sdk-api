---
UID: NF:netfw.INetFwRule.put_EdgeTraversal
title: INetFwRule::put_EdgeTraversal (netfw.h)
description: Indicates whether edge traversal is enabled or disabled for this rule. (Put)
helpviewer_keywords: ["EdgeTraversal property [ICS/ICF]","EdgeTraversal property [ICS/ICF]","INetFwRule interface","INetFwRule interface [ICS/ICF]","EdgeTraversal property","INetFwRule.EdgeTraversal","INetFwRule.put_EdgeTraversal","INetFwRule::EdgeTraversal","INetFwRule::get_EdgeTraversal","INetFwRule::put_EdgeTraversal","ics.inetfwrule_edgetraversal","netfw/INetFwRule::EdgeTraversal","netfw/INetFwRule::get_EdgeTraversal","netfw/INetFwRule::put_EdgeTraversal","put_EdgeTraversal"]
old-location: ics\inetfwrule_edgetraversal.htm
tech.root: ics
ms.assetid: a45a8161-3273-4d43-86bf-34d1b776dbbc
ms.date: 12/05/2018
ms.keywords: EdgeTraversal property [ICS/ICF], EdgeTraversal property [ICS/ICF],INetFwRule interface, INetFwRule interface [ICS/ICF],EdgeTraversal property, INetFwRule.EdgeTraversal, INetFwRule.put_EdgeTraversal, INetFwRule::EdgeTraversal, INetFwRule::get_EdgeTraversal, INetFwRule::put_EdgeTraversal, ics.inetfwrule_edgetraversal, netfw/INetFwRule::EdgeTraversal, netfw/INetFwRule::get_EdgeTraversal, netfw/INetFwRule::put_EdgeTraversal, put_EdgeTraversal
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
 - INetFwRule::put_EdgeTraversal
 - netfw/INetFwRule::put_EdgeTraversal
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
 - INetFwRule.EdgeTraversal
 - INetFwRule.get_EdgeTraversal
 - INetFwRule.put_EdgeTraversal
---

# INetFwRule::put_EdgeTraversal


## -description

Indicates whether edge traversal is enabled or disabled for this rule.

This property is read/write.

## -parameters

## -remarks

The EdgeTraversal property indicates that specific inbound traffic is allowed to tunnel through NATs and other edge devices using the Teredo tunneling technology.  In order for this setting to work correctly, the application or service with the inbound firewall rule needs to support IPv6.  The primary application of this setting allows listeners on the host to be globally addressable through a Teredo IPv6 address.

New rules have the EdgeTraversal property disabled by default.

Also see the restrictions on changing properties described in the Remarks section of the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> interface page.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a>
