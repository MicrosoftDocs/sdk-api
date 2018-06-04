---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _VDS_LOADBALANCE_POLICY_ENUM enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines a set of valid load balance policies for a path. These policies correspond to the 
   definitions in the DSM MOF.


## -enum-fields




### -field VDS_LBP_UNKNOWN

The policy is unknown.


### -field VDS_LBP_FAILOVER

The policy uses one primary path with other paths being backup paths.


### -field VDS_LBP_ROUND_ROBIN

The policy uses all paths in round-robin fashion.


### -field VDS_LBP_ROUND_ROBIN_WITH_SUBSET

The policy uses primary paths in round-robin fashion. The backup paths are used if all of the primary paths 
     fail.


### -field VDS_LBP_DYN_LEAST_QUEUE_DEPTH

The policy uses the path with the least number of active requests.


### -field VDS_LBP_WEIGHTED_PATHS

The policy uses the path with the least weight (each path is assigned a weight).


### -field VDS_LBP_LEAST_BLOCKS

The policy uses the path with the least blocks.


### -field VDS_LBP_VENDOR_SPECIFIC

The policy is a vendor-specific policy.


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LOADBALANCE_POLICY_ENUM</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LOADBALANCE_POLICY_ENUM</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>
 

 

