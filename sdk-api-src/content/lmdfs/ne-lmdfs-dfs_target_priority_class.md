---
UID: NE:lmdfs._DFS_TARGET_PRIORITY_CLASS
title: DFS_TARGET_PRIORITY_CLASS
author: windows-sdk-content
description: Defines the set of possible DFS target priority class settings.
old-location: dfs\dfs_target_priority_class.htm
tech.root: Dfs
ms.assetid: 4aac4575-630f-4cb6-8312-edd1fad8f128
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DFS_TARGET_PRIORITY_CLASS, DFS_TARGET_PRIORITY_CLASS enumeration [Distributed File System], DfsGlobalHighPriorityClass, DfsGlobalLowPriorityClass, DfsInvalidPriorityClass, DfsSiteCostHighPriorityClass, DfsSiteCostLowPriorityClass, DfsSiteCostNormalPriorityClass, dfs.dfs_target_priority_class, fs.dfs_target_priority_class, lmdfs/DFS_TARGET_PRIORITY_CLASS, lmdfs/DfsGlobalHighPriorityClass, lmdfs/DfsGlobalLowPriorityClass, lmdfs/DfsInvalidPriorityClass, lmdfs/DfsSiteCostHighPriorityClass, lmdfs/DfsSiteCostLowPriorityClass, lmdfs/DfsSiteCostNormalPriorityClass, netmgmt.dfs_target_priority_class
ms.topic: enum
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008, Windows Server 2008
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LmDfs.h
api_name:
 - DFS_TARGET_PRIORITY_CLASS
product: Windows
targetos: Windows
req.typenames: DFS_TARGET_PRIORITY_CLASS
req.redist: 
---

# DFS_TARGET_PRIORITY_CLASS enumeration


## -description


Defines the set of possible DFS target priority class settings.


## -enum-fields




### -field DfsInvalidPriorityClass

The priority class is not valid.


### -field DfsSiteCostNormalPriorityClass

The middle or "normal" site cost priority class for a DFS target.


### -field DfsGlobalHighPriorityClass

The highest priority class for a DFS target. Targets assigned this class receive global preference.


### -field DfsSiteCostHighPriorityClass

The highest site cost priority class for a DFS target. Targets assigned this class receive the most 
      preference among targets of the same site cost for a given DFS client.


### -field DfsSiteCostLowPriorityClass

The lowest site cost priority class for a DFS target. Targets assigned this class receive the least 
      preference among targets of the same site cost for a given DFS client.


### -field DfsGlobalLowPriorityClass

The lowest level of priority class for a DFS target. Targets assigned this class receive the least 
      preference globally.


### -field v1_enum




## -remarks



The order of priority classes from highest to lowest is as follows:

<ul>
<li><b>DfsGlobalHighPriorityClass</b></li>
<li><b>DfsSiteCostHighPriorityClass</b></li>
<li><b>DfsSiteCostNormalPriorityClass</b></li>
<li><b>DfsSiteCostLowPriorityClass</b></li>
<li><b>DfsGlobalLowPriorityClass</b></li>
</ul>
Server targets are initially grouped into global high priority, normal priority, and low priority classes. The 
     normal priority class is then subdivided, based on Active Directory site cost, into site-cost high priority, 
     site-cost normal priority, and site-cost low priority classes.

For example, all of the server targets with a site-cost value of 0 are first grouped into site-cost high, 
     normal, and low priority classes. Then, all server targets with lower site costs are likewise separated into 
     site-cost high, normal, and low priority classes. Thus, a server target with a site-cost value of 0 and a 
     site-cost low priority class is still ranked higher than a server target with a site-cost value of 1 and 
     site-cost high priority class.

For more information about how server target priority is determined, see 
     <a href="https://msdn.microsoft.com/0aacebf7-49cc-4287-a5c4-0d25a416d227">DFS Server Target Prioritization</a>.




## -see-also




<a href="https://msdn.microsoft.com/0aacebf7-49cc-4287-a5c4-0d25a416d227">DFS Server Target Prioritization</a>
 

 

