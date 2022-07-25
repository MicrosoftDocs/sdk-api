---
UID: NE:lmdfs._DFS_TARGET_PRIORITY_CLASS~r1
title: DFS_TARGET_PRIORITY_CLASS
ms.date: 01/30/2019
ms.keywords: _DFS_TARGET_PRIORITY_CLASS, DFS_TARGET_PRIORITY_CLASS
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: lmdfs.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: 
req.umdf-ver: 
f1_keywords:
 - _DFS_TARGET_PRIORITY_CLASS
 - lmdfs/_DFS_TARGET_PRIORITY_CLASS
 - DFS_TARGET_PRIORITY_CLASS
 - lmdfs/DFS_TARGET_PRIORITY_CLASS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - lmdfs.h
api_name:
 - _DFS_TARGET_PRIORITY_CLASS
 - DFS_TARGET_PRIORITY_CLASS
---

# DFS_TARGET_PRIORITY_CLASS enumeration


## -description

Defines the set of possible DFS target priority class settings.

## -enum-fields

### -field DfsInvalidPriorityClass:-1

The priority class is not valid.

### -field DfsSiteCostNormalPriorityClass:0

The middle or "normal" site cost priority class for a DFS target.

### -field DfsGlobalHighPriorityClass

The highest priority class for a DFS target. Targets assigned this class receive global preference.

### -field DfsSiteCostHighPriorityClass

The highest site cost priority class for a DFS target. Targets assigned this class receive the most preference among targets of the same site cost for a given DFS client.

### -field DfsSiteCostLowPriorityClass

The lowest site cost priority class for a DFS target. Targets assigned this class receive the least preference among targets of the same site cost for a given DFS client.

### -field DfsGlobalLowPriorityClass

The lowest level of priority class for a DFS target. Targets assigned this class receive the least preference globally.

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
     <a href="/previous-versions/windows/desktop/dfs/dfs-server-target-prioritization">DFS Server Target Prioritization</a>.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/dfs-server-target-prioritization">DFS Server Target Prioritization</a>
