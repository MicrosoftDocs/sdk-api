---
UID: NF:netfw.INetFwRule.get_Interfaces
title: INetFwRule::get_Interfaces (netfw.h)
description: Specifies the list of interfaces for which the rule applies. (Get)
helpviewer_keywords: ["INetFwRule interface [ICS/ICF]","Interfaces property","INetFwRule.Interfaces","INetFwRule.get_Interfaces","INetFwRule::Interfaces","INetFwRule::get_Interfaces","INetFwRule::put_Interfaces","Interfaces property [ICS/ICF]","Interfaces property [ICS/ICF]","INetFwRule interface","get_Interfaces","ics.inetfwrule_interfaces","netfw/INetFwRule::Interfaces","netfw/INetFwRule::get_Interfaces","netfw/INetFwRule::put_Interfaces"]
old-location: ics\inetfwrule_interfaces.htm
tech.root: ics
ms.assetid: f04ac143-bbb7-4676-936e-4282ebf58f56
ms.date: 12/05/2018
ms.keywords: INetFwRule interface [ICS/ICF],Interfaces property, INetFwRule.Interfaces, INetFwRule.get_Interfaces, INetFwRule::Interfaces, INetFwRule::get_Interfaces, INetFwRule::put_Interfaces, Interfaces property [ICS/ICF], Interfaces property [ICS/ICF],INetFwRule interface, get_Interfaces, ics.inetfwrule_interfaces, netfw/INetFwRule::Interfaces, netfw/INetFwRule::get_Interfaces, netfw/INetFwRule::put_Interfaces
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
 - INetFwRule::get_Interfaces
 - netfw/INetFwRule::get_Interfaces
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
 - INetFwRule.Interfaces
 - INetFwRule.get_Interfaces
 - INetFwRule.put_Interfaces
---

# INetFwRule::get_Interfaces


## -description

Specifies the list of interfaces for which  the rule applies.

This property is read/write.

## -parameters

## -remarks

This property is optional.  The interfaces in the list are represented by their friendly name. 

Also see the restrictions on changing properties described in the Remarks section of the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> interface page.

## -see-also

<a href="/previous-versions/windows/desktop/ics/c-adding-a-per-interface-rule">Adding a Per Interface Rule</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a>
