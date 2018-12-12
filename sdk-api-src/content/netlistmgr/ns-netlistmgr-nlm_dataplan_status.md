---
UID: NS:netlistmgr.NLM_DATAPLAN_STATUS
title: NLM_DATAPLAN_STATUS
author: windows-sdk-content
description: NLM_DATAPLAN_STATUS structure stores the current data plan status information supplied by the carrier.
old-location: nla\nlm_dataplan_status.htm
tech.root: nla
ms.assetid: 49774150-FD7E-4541-95DF-C848247A6A9C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NLM_DATAPLAN_STATUS, NLM_DATAPLAN_STATUS structure [Network Awareness], PNLM_DATAPLAN_STATUS, PNLM_DATAPLAN_STATUS structure pointer [Network Awareness], netlistmgr/NLM_DATAPLAN_STATUS, netlistmgr/PNLM_DATAPLAN_STATUS, nla.nlm_dataplan_status
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netlistmgr.h
api_name:
 - NLM_DATAPLAN_STATUS
product: Windows
targetos: Windows
req.typenames: NLM_DATAPLAN_STATUS
req.redist: 
---

# NLM_DATAPLAN_STATUS structure


## -description


The <b>NLM_DATAPLAN_STATUS</b> structure stores the current data plan status information supplied by the carrier.


## -struct-fields




### -field InterfaceGuid

The unique ID of the interface associated with the data plan. This GUID is determined by the system when a data plan is first used by a system connection.


### -field UsageData

An <a href="https://msdn.microsoft.com/1D917CD0-4D71-4780-9720-A1F3FDCBBB16">NLM_USAGE_DATA</a> structure containing  current data usage value expressed in megabytes, as well as the  system time at the moment this value was last synced. 

If this value is not supplied, <a href="https://msdn.microsoft.com/1D917CD0-4D71-4780-9720-A1F3FDCBBB16">NLM_USAGE_DATA</a> will indicate <b>NLM_UNKNOWN_DATAPLAN_STATUS</b> for <b>UsageInMegabytes</b> and a value of '0' will be set for <b>LastSyncTime.</b>


### -field DataLimitInMegabytes

The data plan usage limit expressed in megabytes. If this value is not supplied, a default value of <b>NLM_UNKNOWN_DATAPLAN_STATUS</b> is set.


### -field InboundBandwidthInKbps

The maximum inbound connection bandwidth expressed in kbps. If this value is not supplied, a default value of <b>NLM_UNKNOWN_DATAPLAN_STATUS</b> is set.


### -field OutboundBandwidthInKbps

The maximum outbound connection bandwidth expressed in kbps. If this value is not supplied, a default value of <b>NLM_UNKNOWN_DATAPLAN_STATUS</b> is set.


### -field NextBillingCycle

The start time of the next billing cycle. If this value is not supplied, a default value of '0' is set.


### -field MaxTransferSizeInMegabytes

The maximum suggested transfer size for this network expressed in megabytes. If this value is not supplied, a default value of <b>NLM_UNKNOWN_DATAPLAN_STATUS</b> is set.


### -field Reserved

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/861ED7D2-569A-4B62-BAB6-CA649CA9B524">INetworkConnectionCost::GetDataPlanStatus</a>



<a href="https://msdn.microsoft.com/A9908F22-A9E9-4C05-A434-57D0C433EA3E">INetworkCostManagerEvents::DataPlanStatusChanged</a>



<a href="https://msdn.microsoft.com/1D917CD0-4D71-4780-9720-A1F3FDCBBB16">NLM_USAGE_DATA</a>
 

 

