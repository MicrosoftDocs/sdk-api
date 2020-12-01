---
UID: NF:netfw.INetFwPolicy.get_CurrentProfile
title: INetFwPolicy::get_CurrentProfile (netfw.h)
description: Retrieves the current firewall profile.
helpviewer_keywords: ["CurrentProfile property [ICS/ICF]","CurrentProfile property [ICS/ICF]","INetFwPolicy interface","INetFwPolicy interface [ICS/ICF]","CurrentProfile property","INetFwPolicy.CurrentProfile","INetFwPolicy.get_CurrentProfile","INetFwPolicy::CurrentProfile","INetFwPolicy::get_CurrentProfile","get_CurrentProfile","ics.inetfwpolicy_currentprofile","netfw/INetFwPolicy::CurrentProfile","netfw/INetFwPolicy::get_CurrentProfile"]
old-location: ics\inetfwpolicy_currentprofile.htm
tech.root: ics
ms.assetid: 2ee59a3e-a4e3-4714-aba7-9d72bfacfb34
ms.date: 12/05/2018
ms.keywords: CurrentProfile property [ICS/ICF], CurrentProfile property [ICS/ICF],INetFwPolicy interface, INetFwPolicy interface [ICS/ICF],CurrentProfile property, INetFwPolicy.CurrentProfile, INetFwPolicy.get_CurrentProfile, INetFwPolicy::CurrentProfile, INetFwPolicy::get_CurrentProfile, get_CurrentProfile, ics.inetfwpolicy_currentprofile, netfw/INetFwPolicy::CurrentProfile, netfw/INetFwPolicy::get_CurrentProfile
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
 - INetFwPolicy::get_CurrentProfile
 - netfw/INetFwPolicy::get_CurrentProfile
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
 - INetFwPolicy.CurrentProfile
 - INetFwPolicy.get_CurrentProfile
---

# INetFwPolicy::get_CurrentProfile


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Retrieves the current firewall profile.

This property is read-only.

## -parameters

## -remarks

The SharedAccess service must be running.

To get specific profile objects, use <a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwpolicy-getprofilebytype">INetFwPolicy::GetProfileByType</a> instead of <b>INetFwPolicy::CurrentProfile</b>.

On Windows 7, the netsh context <b>current</b> maps to all currently active profiles for netsh advfirewall and netsh firewall. On earlier versions of Windows, <b>current</b> maps to the most restrictive profile.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwmgr">INetFwMgr</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy">INetFwPolicy</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwprofile">INetFwProfile</a>