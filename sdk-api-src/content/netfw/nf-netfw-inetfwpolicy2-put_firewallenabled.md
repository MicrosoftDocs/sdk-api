---
UID: NF:netfw.INetFwPolicy2.put_FirewallEnabled
title: INetFwPolicy2::put_FirewallEnabled (netfw.h)
description: Indicates whether a firewall is enabled locally (the effective result may differ due to group policy settings). (Put)
helpviewer_keywords: ["FirewallEnabled property [ICS/ICF]","FirewallEnabled property [ICS/ICF]","INetFwPolicy2 interface","INetFwPolicy2 interface [ICS/ICF]","FirewallEnabled property","INetFwPolicy2.FirewallEnabled","INetFwPolicy2.put_FirewallEnabled","INetFwPolicy2::FirewallEnabled","INetFwPolicy2::get_FirewallEnabled","INetFwPolicy2::put_FirewallEnabled","ics.inetfwpolicy2_firewallenabled","netfw/INetFwPolicy2::FirewallEnabled","netfw/INetFwPolicy2::get_FirewallEnabled","netfw/INetFwPolicy2::put_FirewallEnabled","put_FirewallEnabled"]
old-location: ics\inetfwpolicy2_firewallenabled.htm
tech.root: ics
ms.assetid: 6c3ca9dd-a562-454f-bb9a-856beba772f3
ms.date: 12/05/2018
ms.keywords: FirewallEnabled property [ICS/ICF], FirewallEnabled property [ICS/ICF],INetFwPolicy2 interface, INetFwPolicy2 interface [ICS/ICF],FirewallEnabled property, INetFwPolicy2.FirewallEnabled, INetFwPolicy2.put_FirewallEnabled, INetFwPolicy2::FirewallEnabled, INetFwPolicy2::get_FirewallEnabled, INetFwPolicy2::put_FirewallEnabled, ics.inetfwpolicy2_firewallenabled, netfw/INetFwPolicy2::FirewallEnabled, netfw/INetFwPolicy2::get_FirewallEnabled, netfw/INetFwPolicy2::put_FirewallEnabled, put_FirewallEnabled
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
 - INetFwPolicy2::put_FirewallEnabled
 - netfw/INetFwPolicy2::put_FirewallEnabled
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
 - INetFwPolicy2.FirewallEnabled
 - INetFwPolicy2.get_FirewallEnabled
 - INetFwPolicy2.put_FirewallEnabled
---

# INetFwPolicy2::put_FirewallEnabled


## -description

Indicates whether a firewall is enabled locally (the effective result may differ due to group policy settings).

This property is read/write.

## -parameters

## -remarks

When you pass a profile type obtained from the <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_currentprofiletypes">CurrentProfileTypes</a> property, make sure that you pass only one profile type to <b>get_FirewallEnabled</b> and <b>put_FirewallEnabled</b>. Note that <b>get_CurrentProfileTypes</b> can return multiple profiles.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2">INetFwPolicy2</a>
