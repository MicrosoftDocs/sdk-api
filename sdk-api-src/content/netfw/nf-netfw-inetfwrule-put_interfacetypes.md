---
UID: NF:netfw.INetFwRule.put_InterfaceTypes
title: INetFwRule::put_InterfaceTypes (netfw.h)
description: Specifies the list of interface types for which the rule applies. (Put)
helpviewer_keywords: ["INetFwRule interface [ICS/ICF]","InterfaceTypes property","INetFwRule.InterfaceTypes","INetFwRule.put_InterfaceTypes","INetFwRule::InterfaceTypes","INetFwRule::get_InterfaceTypes","INetFwRule::put_InterfaceTypes","InterfaceTypes property [ICS/ICF]","InterfaceTypes property [ICS/ICF]","INetFwRule interface","ics.inetfwrule_interfacetypes","netfw/INetFwRule::InterfaceTypes","netfw/INetFwRule::get_InterfaceTypes","netfw/INetFwRule::put_InterfaceTypes","put_InterfaceTypes"]
old-location: ics\inetfwrule_interfacetypes.htm
tech.root: ics
ms.assetid: 2548875c-3c23-4076-9d3d-82bebf5e7718
ms.date: 12/05/2018
ms.keywords: INetFwRule interface [ICS/ICF],InterfaceTypes property, INetFwRule.InterfaceTypes, INetFwRule.put_InterfaceTypes, INetFwRule::InterfaceTypes, INetFwRule::get_InterfaceTypes, INetFwRule::put_InterfaceTypes, InterfaceTypes property [ICS/ICF], InterfaceTypes property [ICS/ICF],INetFwRule interface, ics.inetfwrule_interfacetypes, netfw/INetFwRule::InterfaceTypes, netfw/INetFwRule::get_InterfaceTypes, netfw/INetFwRule::put_InterfaceTypes, put_InterfaceTypes
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
 - INetFwRule::put_InterfaceTypes
 - netfw/INetFwRule::put_InterfaceTypes
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
 - INetFwRule.InterfaceTypes
 - INetFwRule.get_InterfaceTypes
 - INetFwRule.put_InterfaceTypes
---

# INetFwRule::put_InterfaceTypes


## -description

Specifies the list of interface types for which the rule applies.

This property is read/write.

## -parameters

## -remarks

This property is optional.

Also see the restrictions on changing properties described in the Remarks section of the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> interface page.

Acceptable values for this property are "RemoteAccess", "Wireless", "Lan", and "All". If more than one interface type is specified, the strings must be separated by a comma.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a>
