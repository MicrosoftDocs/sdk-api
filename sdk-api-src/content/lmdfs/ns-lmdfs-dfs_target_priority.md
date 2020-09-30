---
UID: NS:lmdfs._DFS_TARGET_PRIORITY
title: DFS_TARGET_PRIORITY (lmdfs.h)
description: Contains the priority class and rank of a specific DFS target.
helpviewer_keywords: ["*PDFS_TARGET_PRIORITY","DFS_TARGET_PRIORITY","DFS_TARGET_PRIORITY structure [Distributed File System]","LPDFS_TARGET_PRIORITY","LPDFS_TARGET_PRIORITY structure pointer [Distributed File System]","PDFS_TARGET_PRIORITY","PDFS_TARGET_PRIORITY structure pointer [Distributed File System]","dfs.dfs_target_priority","fs.dfs_target_priority","lmdfs/DFS_TARGET_PRIORITY","lmdfs/LPDFS_TARGET_PRIORITY","lmdfs/PDFS_TARGET_PRIORITY","netmgmt.dfs_target_priority"]
old-location: dfs\dfs_target_priority.htm
tech.root: Dfs
ms.assetid: b8f645ab-e3b4-4e0f-809a-57e27ab1e641
ms.date: 12/05/2018
ms.keywords: '*PDFS_TARGET_PRIORITY, DFS_TARGET_PRIORITY, DFS_TARGET_PRIORITY structure [Distributed File System], LPDFS_TARGET_PRIORITY, LPDFS_TARGET_PRIORITY structure pointer [Distributed File System], PDFS_TARGET_PRIORITY, PDFS_TARGET_PRIORITY structure pointer [Distributed File System], dfs.dfs_target_priority, fs.dfs_target_priority, lmdfs/DFS_TARGET_PRIORITY, lmdfs/LPDFS_TARGET_PRIORITY, lmdfs/PDFS_TARGET_PRIORITY, netmgmt.dfs_target_priority'
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
targetos: Windows
req.typenames: DFS_TARGET_PRIORITY, *PDFS_TARGET_PRIORITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DFS_TARGET_PRIORITY
 - lmdfs/_DFS_TARGET_PRIORITY
 - PDFS_TARGET_PRIORITY
 - lmdfs/PDFS_TARGET_PRIORITY
 - DFS_TARGET_PRIORITY
 - lmdfs/DFS_TARGET_PRIORITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LmDfs.h
api_name:
 - DFS_TARGET_PRIORITY
---

# DFS_TARGET_PRIORITY structure


## -description

Contains the priority class and rank of a specific DFS target.

## -struct-fields

### -field TargetPriorityClass

<a href="/windows/win32/api/lmdfs/ne-lmdfs-dfs_target_priority_class~r1">DFS_TARGET_PRIORITY_CLASS</a> enumeration 
      value that specifies the priority class of the target.

### -field TargetPriorityRank

Specifies the priority rank value of the target. The default value is 0, which indicates the highest 
      priority rank within a priority class.

### -field Reserved

This member is reserved and must be zero.

## -remarks

This structure is used as the <b>TargetPriority</b> member of the 
    <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104">DFS_INFO_104</a>, 
    <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106">DFS_INFO_106</a>, and 
    <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1">DFS_STORAGE_INFO_1</a> structures. There are no functions 
    that use this structure directly.

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
    normal, and low priority classes. Then, all server targets with higher site costs are likewise separated into 
    site-cost high, normal, and low priority classes. Thus, a server target with a site-cost value of 0 and a 
    site-cost low priority class is still ranked higher than a server target with a site-cost value of 1 and site-cost 
    high priority class.

Note that the value for a "normal priority class" is set to 0 even though it is lower in priority than 
    <b>DfsGlobalHighPriorityClass</b> and <b>DfsSiteCostHighPriorityClass</b>. This is the default 
    setting for priority class.  Priority rank can be used to discriminate within a priority class for added 
    granularity.

For more information about how server target priority is determined, see 
    <a href="/previous-versions/windows/desktop/dfs/dfs-server-target-prioritization">DFS Server Target Prioritization</a>.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/dfs-server-target-prioritization">DFS Server Target Prioritization</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104">DFS_INFO_104</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106">DFS_INFO_106</a>



<a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1">DFS_STORAGE_INFO_1</a>



<a href="/windows/win32/api/lmdfs/ne-lmdfs-dfs_target_priority_class~r1">DFS_TARGET_PRIORITY_CLASS</a>



<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo">NetDfsSetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>