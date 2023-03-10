---
UID: NF:netfw.INetFwProfile.put_FirewallEnabled
title: INetFwProfile::put_FirewallEnabled (netfw.h)
description: Indicates whether the firewall is enabled. (Put)
helpviewer_keywords: ["FirewallEnabled property [ICS/ICF]","FirewallEnabled property [ICS/ICF]","INetFwProfile interface","INetFwProfile interface [ICS/ICF]","FirewallEnabled property","INetFwProfile.FirewallEnabled","INetFwProfile.put_FirewallEnabled","INetFwProfile::FirewallEnabled","INetFwProfile::get_FirewallEnabled","INetFwProfile::put_FirewallEnabled","ics.inetfwprofile_firewallenabled","netfw/INetFwProfile::FirewallEnabled","netfw/INetFwProfile::get_FirewallEnabled","netfw/INetFwProfile::put_FirewallEnabled","put_FirewallEnabled"]
old-location: ics\inetfwprofile_firewallenabled.htm
tech.root: ics
ms.assetid: cde6327d-e3ae-418f-9e8c-76288c120ca0
ms.date: 12/05/2018
ms.keywords: FirewallEnabled property [ICS/ICF], FirewallEnabled property [ICS/ICF],INetFwProfile interface, INetFwProfile interface [ICS/ICF],FirewallEnabled property, INetFwProfile.FirewallEnabled, INetFwProfile.put_FirewallEnabled, INetFwProfile::FirewallEnabled, INetFwProfile::get_FirewallEnabled, INetFwProfile::put_FirewallEnabled, ics.inetfwprofile_firewallenabled, netfw/INetFwProfile::FirewallEnabled, netfw/INetFwProfile::get_FirewallEnabled, netfw/INetFwProfile::put_FirewallEnabled, put_FirewallEnabled
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
 - INetFwProfile::put_FirewallEnabled
 - netfw/INetFwProfile::put_FirewallEnabled
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
 - INetFwProfile.FirewallEnabled
 - INetFwProfile.get_FirewallEnabled
 - INetFwProfile.put_FirewallEnabled
---

# INetFwProfile::put_FirewallEnabled


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Indicates whether the firewall is enabled.

This property is read/write.

## -parameters

## -remarks

 The resulting  firewall status is based on the local policy from the local store. Use the procedure <a href="/previous-versions/windows/desktop/ics/checking-the-effective-firewall-status">Checking the Effective Firewall Status</a> to determine the overall operational state.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwprofile">INetFwProfile</a>
