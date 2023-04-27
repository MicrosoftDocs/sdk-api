---
UID: NF:netfw.INetFwPolicy2.get_DefaultOutboundAction
title: INetFwPolicy2::get_DefaultOutboundAction (netfw.h)
description: Specifies the default action for outbound traffic. These settings are Allow by default. (Get)
helpviewer_keywords: ["DefaultOutboundAction property [ICS/ICF]","DefaultOutboundAction property [ICS/ICF]","INetFwPolicy2 interface","INetFwPolicy2 interface [ICS/ICF]","DefaultOutboundAction property","INetFwPolicy2.DefaultOutboundAction","INetFwPolicy2.get_DefaultOutboundAction","INetFwPolicy2::DefaultOutboundAction","INetFwPolicy2::get_DefaultOutboundAction","INetFwPolicy2::put_DefaultOutboundAction","get_DefaultOutboundAction","ics.inetfwpolicy2_defaultoutboundaction","netfw/INetFwPolicy2::DefaultOutboundAction","netfw/INetFwPolicy2::get_DefaultOutboundAction","netfw/INetFwPolicy2::put_DefaultOutboundAction"]
old-location: ics\inetfwpolicy2_defaultoutboundaction.htm
tech.root: ics
ms.assetid: 428f8f74-b2b3-4441-accf-be0b877e7c8b
ms.date: 12/05/2018
ms.keywords: DefaultOutboundAction property [ICS/ICF], DefaultOutboundAction property [ICS/ICF],INetFwPolicy2 interface, INetFwPolicy2 interface [ICS/ICF],DefaultOutboundAction property, INetFwPolicy2.DefaultOutboundAction, INetFwPolicy2.get_DefaultOutboundAction, INetFwPolicy2::DefaultOutboundAction, INetFwPolicy2::get_DefaultOutboundAction, INetFwPolicy2::put_DefaultOutboundAction, get_DefaultOutboundAction, ics.inetfwpolicy2_defaultoutboundaction, netfw/INetFwPolicy2::DefaultOutboundAction, netfw/INetFwPolicy2::get_DefaultOutboundAction, netfw/INetFwPolicy2::put_DefaultOutboundAction
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
 - INetFwPolicy2::get_DefaultOutboundAction
 - netfw/INetFwPolicy2::get_DefaultOutboundAction
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
 - INetFwPolicy2.DefaultOutboundAction
 - INetFwPolicy2.get_DefaultOutboundAction
 - INetFwPolicy2.put_DefaultOutboundAction
---

# INetFwPolicy2::get_DefaultOutboundAction


## -description

Specifies the default action for outbound traffic. These settings are Allow by default.

This property is read/write.

## -parameters

## -remarks

All interfaces are firewall-enabled. This means that all the exceptions (such as GloballyOpenPorts, Applications, or Services) which are  specified in the profile are ignored
   and only locally-initiated traffic is allowed.

When you pass a profile type obtained from the <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_currentprofiletypes">CurrentProfileTypes</a> property, make sure that you pass only one profile type to <b>get_DefaultOutboundAction</b> and <b>put_DefaultOutboundAction</b>. Note that <b>get_CurrentProfileTypes</b> can return multiple profiles.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2">INetFwPolicy2</a>
