---
UID: NF:netfw.INetFwMgr.get_CurrentProfileType
title: INetFwMgr::get_CurrentProfileType (netfw.h)
description: Retrieves the type of firewall profile currently in effect.
helpviewer_keywords: ["CurrentProfileType property [ICS/ICF]","CurrentProfileType property [ICS/ICF]","INetFwMgr interface","INetFwMgr interface [ICS/ICF]","CurrentProfileType property","INetFwMgr.CurrentProfileType","INetFwMgr.get_CurrentProfileType","INetFwMgr::CurrentProfileType","INetFwMgr::get_CurrentProfileType","get_CurrentProfileType","ics.inetfwmgr_currentprofiletype","netfw/INetFwMgr::CurrentProfileType","netfw/INetFwMgr::get_CurrentProfileType"]
old-location: ics\inetfwmgr_currentprofiletype.htm
tech.root: ics
ms.assetid: fa6d79a8-37e4-4172-a6be-3ca803c0feca
ms.date: 12/05/2018
ms.keywords: CurrentProfileType property [ICS/ICF], CurrentProfileType property [ICS/ICF],INetFwMgr interface, INetFwMgr interface [ICS/ICF],CurrentProfileType property, INetFwMgr.CurrentProfileType, INetFwMgr.get_CurrentProfileType, INetFwMgr::CurrentProfileType, INetFwMgr::get_CurrentProfileType, get_CurrentProfileType, ics.inetfwmgr_currentprofiletype, netfw/INetFwMgr::CurrentProfileType, netfw/INetFwMgr::get_CurrentProfileType
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
 - INetFwMgr::get_CurrentProfileType
 - netfw/INetFwMgr::get_CurrentProfileType
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
 - INetFwMgr.CurrentProfileType
 - INetFwMgr.get_CurrentProfileType
---

# INetFwMgr::get_CurrentProfileType


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Retrieves the type of firewall profile currently in effect.

This property is read-only.

## -parameters

## -remarks

The SharedAccess service must be running.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwmgr">INetFwMgr</a>



<a href="/windows/desktop/api/icftypes/ne-icftypes-net_fw_profile_type">NET_FW_PROFILE_TYPE</a>