---
UID: NS:netlistmgr.NLM_SIMULATED_PROFILE_INFO
title: NLM_SIMULATED_PROFILE_INFO (netlistmgr.h)
description: Used to specify values that are used by SetSimulatedProfileInfo to override current internet connection profile values in an RDP Child Session to support the simulation of specific metered internet connection conditions.
helpviewer_keywords: ["NLM_SIMULATED_PROFILE_INFO","NLM_SIMULATED_PROFILE_INFO structure [Network Awareness]","PNLM_SIMULATED_PROFILE_INFO","PNLM_SIMULATED_PROFILE_INFO structure pointer [Network Awareness]","netlistmgr/NLM_SIMULATED_PROFILE_INFO","netlistmgr/PNLM_SIMULATED_PROFILE_INFO","nla.nlm_simulated_profile_info"]
old-location: nla\nlm_simulated_profile_info.htm
tech.root: nla
ms.assetid: 1DC80EB0-E63A-4352-8269-D795E1573851
ms.date: 12/05/2018
ms.keywords: NLM_SIMULATED_PROFILE_INFO, NLM_SIMULATED_PROFILE_INFO structure [Network Awareness], PNLM_SIMULATED_PROFILE_INFO, PNLM_SIMULATED_PROFILE_INFO structure pointer [Network Awareness], netlistmgr/NLM_SIMULATED_PROFILE_INFO, netlistmgr/PNLM_SIMULATED_PROFILE_INFO, nla.nlm_simulated_profile_info
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Netlistmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NLM_SIMULATED_PROFILE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NLM_SIMULATED_PROFILE_INFO
 - netlistmgr/NLM_SIMULATED_PROFILE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netlistmgr.h
api_name:
 - NLM_SIMULATED_PROFILE_INFO
---

# NLM_SIMULATED_PROFILE_INFO structure


## -description

Used to specify values that are used by <a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-setsimulatedprofileinfo">SetSimulatedProfileInfo</a> to override current internet connection profile values in an RDP Child Session to support the simulation of specific metered internet connection conditions.

## -struct-fields

### -field ProfileName

Name for the simulated profile.

### -field cost

The network cost. Possible values are defined by <a href="/windows/desktop/api/netlistmgr/ne-netlistmgr-nlm_connection_cost">NLM_CONNECTION_COST</a>.

### -field UsageInMegabytes

The data usage.

### -field DataLimitInMegabytes

The data limit of the plan.

## -see-also

<a href="/windows/desktop/TermServ/child-sessions">Child Sessions (Windows)</a>



<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-clearsimulatedprofileinfo">ClearSimulatedProfileInfo</a>



<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworklistmanager-setsimulatedprofileinfo">SetSimulatedProfileInfo</a>