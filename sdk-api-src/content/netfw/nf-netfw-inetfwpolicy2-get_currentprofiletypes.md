---
UID: NF:netfw.INetFwPolicy2.get_CurrentProfileTypes
title: INetFwPolicy2::get_CurrentProfileTypes (netfw.h)
description: Retrieves the currently active firewall profile.
helpviewer_keywords: ["CurrentProfileTypes property [ICS/ICF]","CurrentProfileTypes property [ICS/ICF]","INetFwPolicy2 interface","INetFwPolicy2 interface [ICS/ICF]","CurrentProfileTypes property","INetFwPolicy2.CurrentProfileTypes","INetFwPolicy2.get_CurrentProfileTypes","INetFwPolicy2::CurrentProfileTypes","INetFwPolicy2::get_CurrentProfileTypes","get_CurrentProfileTypes","ics.inetfwpolicy2_currentprofiletypes","netfw/INetFwPolicy2::CurrentProfileTypes","netfw/INetFwPolicy2::get_CurrentProfileTypes"]
old-location: ics\inetfwpolicy2_currentprofiletypes.htm
tech.root: ics
ms.assetid: 93f4b508-30db-45a9-a7aa-df4a993dc50b
ms.date: 12/05/2018
ms.keywords: CurrentProfileTypes property [ICS/ICF], CurrentProfileTypes property [ICS/ICF],INetFwPolicy2 interface, INetFwPolicy2 interface [ICS/ICF],CurrentProfileTypes property, INetFwPolicy2.CurrentProfileTypes, INetFwPolicy2.get_CurrentProfileTypes, INetFwPolicy2::CurrentProfileTypes, INetFwPolicy2::get_CurrentProfileTypes, get_CurrentProfileTypes, ics.inetfwpolicy2_currentprofiletypes, netfw/INetFwPolicy2::CurrentProfileTypes, netfw/INetFwPolicy2::get_CurrentProfileTypes
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
 - INetFwPolicy2::get_CurrentProfileTypes
 - netfw/INetFwPolicy2::get_CurrentProfileTypes
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
 - INetFwPolicy2.CurrentProfileTypes
 - INetFwPolicy2.get_CurrentProfileTypes
---

# INetFwPolicy2::get_CurrentProfileTypes


## -description

Retrieves the currently active firewall profile.

This property is read-only.

## -parameters

## -remarks

Multiple profiles can be returned in the profiles bitmask.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2">INetFwPolicy2</a>


<a href="/windows/win32/api/icftypes/ne-icftypes-net_fw_profile_type2">NET_FW_PROFILE_TYPE2</a>