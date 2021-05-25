---
UID: NS:netlistmgr.NLM_USAGE_DATA
title: NLM_USAGE_DATA (netlistmgr.h)
description: NLM_USAGE_DATA structure stores information that indicates the data usage of a plan.
helpviewer_keywords: ["NLM_USAGE_DATA","NLM_USAGE_DATA structure [Network Awareness]","PNLM_USAGE_DATA","PNLM_USAGE_DATA structure pointer [Network Awareness]","netlistmgr/NLM_USAGE_DATA","netlistmgr/PNLM_USAGE_DATA","nla.nlm_usage_data"]
old-location: nla\nlm_usage_data.htm
tech.root: nla
ms.assetid: 1D917CD0-4D71-4780-9720-A1F3FDCBBB16
ms.date: 12/05/2018
ms.keywords: NLM_USAGE_DATA, NLM_USAGE_DATA structure [Network Awareness], PNLM_USAGE_DATA, PNLM_USAGE_DATA structure pointer [Network Awareness], netlistmgr/NLM_USAGE_DATA, netlistmgr/PNLM_USAGE_DATA, nla.nlm_usage_data
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: NLM_USAGE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NLM_USAGE_DATA
 - netlistmgr/NLM_USAGE_DATA
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
 - NLM_USAGE_DATA
---

# NLM_USAGE_DATA structure


## -description

The <b>NLM_USAGE_DATA</b> structure stores information that indicates the data usage  of a plan.

## -struct-fields

### -field UsageInMegabytes

The data usage of a plan, represented in megabytes.

### -field LastSyncTime

The timestamp of last time synced with carriers about the data usage stored in this structure.

## -remarks

If usage is not supplied, <b>UsageInMegabytes</b> is set to <b>NLM_UNKNOWN_DATAPLAN_STATUS</b> (0xFFFFFFFF), and <b>LastSyncTime</b> is set to 0.

## -see-also

<a href="/windows/desktop/api/netlistmgr/nf-netlistmgr-inetworkcostmanager-getdataplanstatus">INetworkCostManager::GetDataPlanStatus</a>



<a href="/windows/desktop/api/netlistmgr/ns-netlistmgr-nlm_dataplan_status">NLM_DATAPLAN_STATUS</a>