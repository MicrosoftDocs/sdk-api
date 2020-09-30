---
UID: NF:netfw.INetFwOpenPort.get_BuiltIn
title: INetFwOpenPort::get_BuiltIn (netfw.h)
description: Indicates whether the port is defined by the system.
helpviewer_keywords: ["BuiltIn property [ICS/ICF]","BuiltIn property [ICS/ICF]","INetFwOpenPort interface","INetFwOpenPort interface [ICS/ICF]","BuiltIn property","INetFwOpenPort.BuiltIn","INetFwOpenPort.get_BuiltIn","INetFwOpenPort::BuiltIn","INetFwOpenPort::get_BuiltIn","get_BuiltIn","ics.inetfwopenport_builtin","netfw/INetFwOpenPort::BuiltIn","netfw/INetFwOpenPort::get_BuiltIn"]
old-location: ics\inetfwopenport_builtin.htm
tech.root: ics
ms.assetid: 7260b9f2-2cbe-4b71-8c99-1d1c30870ae1
ms.date: 12/05/2018
ms.keywords: BuiltIn property [ICS/ICF], BuiltIn property [ICS/ICF],INetFwOpenPort interface, INetFwOpenPort interface [ICS/ICF],BuiltIn property, INetFwOpenPort.BuiltIn, INetFwOpenPort.get_BuiltIn, INetFwOpenPort::BuiltIn, INetFwOpenPort::get_BuiltIn, get_BuiltIn, ics.inetfwopenport_builtin, netfw/INetFwOpenPort::BuiltIn, netfw/INetFwOpenPort::get_BuiltIn
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwOpenPort::get_BuiltIn
 - netfw/INetFwOpenPort::get_BuiltIn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwOpenPort.BuiltIn
 - INetFwOpenPort.get_BuiltIn
---

# INetFwOpenPort::get_BuiltIn


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Indicates whether the port is defined by the system.

This property is read-only.

## -parameters

## -remarks

Ports  with their <b>BuiltIn</b> property set to true (<b>VARIANT_TRUE</b>) are system specified and cannot be removed, only the <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_enabled">Enabled</a>, <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_remoteaddresses">RemoteAddress</a>, and <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwopenport-get_scope">Scope</a> properties can be modified.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwopenport">INetFwOpenPort</a>