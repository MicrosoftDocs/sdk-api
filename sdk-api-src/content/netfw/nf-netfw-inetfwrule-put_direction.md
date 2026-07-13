---
UID: NF:netfw.INetFwRule.put_Direction
title: INetFwRule::put_Direction (netfw.h)
description: Specifies the direction of traffic for which the rule applies. (Put)
helpviewer_keywords: ["Direction property [ICS/ICF]","Direction property [ICS/ICF]","INetFwRule interface","INetFwRule interface [ICS/ICF]","Direction property","INetFwRule.Direction","INetFwRule.put_Direction","INetFwRule::Direction","INetFwRule::get_Direction","INetFwRule::put_Direction","ics.inetfwrule_direction","netfw/INetFwRule::Direction","netfw/INetFwRule::get_Direction","netfw/INetFwRule::put_Direction","put_Direction"]
old-location: ics\inetfwrule_direction.htm
tech.root: ics
ms.assetid: 4462c39a-27b8-497b-8393-ed63c7e4cc9b
ms.date: 12/05/2018
ms.keywords: Direction property [ICS/ICF], Direction property [ICS/ICF],INetFwRule interface, INetFwRule interface [ICS/ICF],Direction property, INetFwRule.Direction, INetFwRule.put_Direction, INetFwRule::Direction, INetFwRule::get_Direction, INetFwRule::put_Direction, ics.inetfwrule_direction, netfw/INetFwRule::Direction, netfw/INetFwRule::get_Direction, netfw/INetFwRule::put_Direction, put_Direction
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
 - INetFwRule::put_Direction
 - netfw/INetFwRule::put_Direction
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
 - INetFwRule.Direction
 - INetFwRule.get_Direction
 - INetFwRule.put_Direction
---

# INetFwRule::put_Direction


## -description

Specifies the direction of traffic for which  the rule applies.

This property is read/write.

## -parameters

## -remarks

This property is optional.  If this property is not specified, the default value is <b>in</b>.

Also see the restrictions on changing properties described in the Remarks section of the <a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a> interface page.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrule">INetFwRule</a>



<a href="/windows/win32/api/icftypes/ne-icftypes-net_fw_rule_direction">NET_FW_RULE_DIRECTION</a>
