---
UID: NF:netfw.INetFwProfile.get_UnicastResponsesToMulticastBroadcastDisabled
title: INetFwProfile::get_UnicastResponsesToMulticastBroadcastDisabled (netfw.h)
description: Indicates whether the firewall should not allow unicast responses to multicast and broadcast traffic. (INetFwProfile.get_UnicastResponsesToMulticastBroadcastDisabled)
helpviewer_keywords: ["INetFwProfile interface [ICS/ICF]","UnicastResponsesToMulticastBroadcastDisabled property","INetFwProfile.UnicastResponsesToMulticastBroadcastDisabled","INetFwProfile.get_UnicastResponsesToMulticastBroadcastDisabled","INetFwProfile::UnicastResponsesToMulticastBroadcastDisabled","INetFwProfile::get_UnicastResponsesToMulticastBroadcastDisabled","INetFwProfile::put_UnicastResponsesToMulticastBroadcastDisabled","UnicastResponsesToMulticastBroadcastDisabled property [ICS/ICF]","UnicastResponsesToMulticastBroadcastDisabled property [ICS/ICF]","INetFwProfile interface","get_UnicastResponsesToMulticastBroadcastDisabled","ics.inetfwprofile_unicastresponsestomulticastbroadcastdisabled","netfw/INetFwProfile::UnicastResponsesToMulticastBroadcastDisabled","netfw/INetFwProfile::get_UnicastResponsesToMulticastBroadcastDisabled","netfw/INetFwProfile::put_UnicastResponsesToMulticastBroadcastDisabled"]
old-location: ics\inetfwprofile_unicastresponsestomulticastbroadcastdisabled.htm
tech.root: ics
ms.assetid: 61a0c65e-8dfa-4f3e-a28f-141a72065123
ms.date: 12/05/2018
ms.keywords: INetFwProfile interface [ICS/ICF],UnicastResponsesToMulticastBroadcastDisabled property, INetFwProfile.UnicastResponsesToMulticastBroadcastDisabled, INetFwProfile.get_UnicastResponsesToMulticastBroadcastDisabled, INetFwProfile::UnicastResponsesToMulticastBroadcastDisabled, INetFwProfile::get_UnicastResponsesToMulticastBroadcastDisabled, INetFwProfile::put_UnicastResponsesToMulticastBroadcastDisabled, UnicastResponsesToMulticastBroadcastDisabled property [ICS/ICF], UnicastResponsesToMulticastBroadcastDisabled property [ICS/ICF],INetFwProfile interface, get_UnicastResponsesToMulticastBroadcastDisabled, ics.inetfwprofile_unicastresponsestomulticastbroadcastdisabled, netfw/INetFwProfile::UnicastResponsesToMulticastBroadcastDisabled, netfw/INetFwProfile::get_UnicastResponsesToMulticastBroadcastDisabled, netfw/INetFwProfile::put_UnicastResponsesToMulticastBroadcastDisabled
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
 - INetFwProfile::get_UnicastResponsesToMulticastBroadcastDisabled
 - netfw/INetFwProfile::get_UnicastResponsesToMulticastBroadcastDisabled
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
 - INetFwProfile.UnicastResponsesToMulticastBroadcastDisabled
 - INetFwProfile.get_UnicastResponsesToMulticastBroadcastDisabled
 - INetFwProfile.put_UnicastResponsesToMulticastBroadcastDisabled
---

# INetFwProfile::get_UnicastResponsesToMulticastBroadcastDisabled


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Indicates whether the firewall should not allow unicast responses to multicast and
   broadcast traffic.

This property is read/write.

## -parameters

## -remarks

If a PC sends a broadcast packet, a unicast response is allowed for three seconds. Use this property to change this behavior.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwprofile">INetFwProfile</a>
