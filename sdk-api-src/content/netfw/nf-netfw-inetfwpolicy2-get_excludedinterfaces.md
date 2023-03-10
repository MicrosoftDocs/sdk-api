---
UID: NF:netfw.INetFwPolicy2.get_ExcludedInterfaces
title: INetFwPolicy2::get_ExcludedInterfaces (netfw.h)
description: Specifies a list of interfaces on which firewall settings are excluded. (Get)
helpviewer_keywords: ["ExcludedInterfaces property [ICS/ICF]","ExcludedInterfaces property [ICS/ICF]","INetFwPolicy2 interface","INetFwPolicy2 interface [ICS/ICF]","ExcludedInterfaces property","INetFwPolicy2.ExcludedInterfaces","INetFwPolicy2.get_ExcludedInterfaces","INetFwPolicy2::ExcludedInterfaces","INetFwPolicy2::get_ExcludedInterfaces","INetFwPolicy2::put_ExcludedInterfaces","get_ExcludedInterfaces","ics.inetfwpolicy2_excludedinterfaces","netfw/INetFwPolicy2::ExcludedInterfaces","netfw/INetFwPolicy2::get_ExcludedInterfaces","netfw/INetFwPolicy2::put_ExcludedInterfaces"]
old-location: ics\inetfwpolicy2_excludedinterfaces.htm
tech.root: ics
ms.assetid: 0e8cbb09-c146-42e9-9b7c-002e6775bf19
ms.date: 12/05/2018
ms.keywords: ExcludedInterfaces property [ICS/ICF], ExcludedInterfaces property [ICS/ICF],INetFwPolicy2 interface, INetFwPolicy2 interface [ICS/ICF],ExcludedInterfaces property, INetFwPolicy2.ExcludedInterfaces, INetFwPolicy2.get_ExcludedInterfaces, INetFwPolicy2::ExcludedInterfaces, INetFwPolicy2::get_ExcludedInterfaces, INetFwPolicy2::put_ExcludedInterfaces, get_ExcludedInterfaces, ics.inetfwpolicy2_excludedinterfaces, netfw/INetFwPolicy2::ExcludedInterfaces, netfw/INetFwPolicy2::get_ExcludedInterfaces, netfw/INetFwPolicy2::put_ExcludedInterfaces
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
 - INetFwPolicy2::get_ExcludedInterfaces
 - netfw/INetFwPolicy2::get_ExcludedInterfaces
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
 - INetFwPolicy2.ExcludedInterfaces
 - INetFwPolicy2.get_ExcludedInterfaces
 - INetFwPolicy2.put_ExcludedInterfaces
---

# INetFwPolicy2::get_ExcludedInterfaces


## -description

Specifies a list of interfaces on which firewall settings are excluded.

This property is read/write.

## -parameters

## -remarks

An excluded interface is an interface to which the firewall is not applicable.  The firewall is not applicable to any traffic received from or sent to an excluded interface. An empty list indicates that there are no excluded interfaces.

When you pass a profile type obtained from the <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy2-get_currentprofiletypes">CurrentProfileTypes</a> property, make sure that you pass only one profile type to <b>get_ExcludedInterfaces</b> and <b>put_ExcludedInterfaces</b>. Note that <b>get_CurrentProfileTypes</b> can return multiple profiles.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2">INetFwPolicy2</a>
