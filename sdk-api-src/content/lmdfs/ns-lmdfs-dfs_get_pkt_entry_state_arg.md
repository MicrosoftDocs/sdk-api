---
UID: NS:lmdfs.DFS_GET_PKT_ENTRY_STATE_ARG
title: DFS_GET_PKT_ENTRY_STATE_ARG (lmdfs.h)
description: Input buffer used with the FSCTL_DFS_GET_PKT_ENTRY_STATE control code.
helpviewer_keywords: ["*PDFS_GET_PKT_ENTRY_STATE_ARG","DFS_GET_PKT_ENTRY_STATE_ARG","DFS_GET_PKT_ENTRY_STATE_ARG structure [Distributed File System]","PDFS_GET_PKT_ENTRY_STATE_ARG","PDFS_GET_PKT_ENTRY_STATE_ARG structure pointer [Distributed File System]","dfs.dfs_get_pkt_entry_state_arg","lmdfs/DFS_GET_PKT_ENTRY_STATE_ARG","lmdfs/PDFS_GET_PKT_ENTRY_STATE_ARG"]
old-location: dfs\dfs_get_pkt_entry_state_arg.htm
tech.root: Dfs
ms.assetid: eb69d346-d88c-48e8-abd7-5cbb5976f41f
ms.date: 12/05/2018
ms.keywords: '*PDFS_GET_PKT_ENTRY_STATE_ARG, DFS_GET_PKT_ENTRY_STATE_ARG, DFS_GET_PKT_ENTRY_STATE_ARG structure [Distributed File System], PDFS_GET_PKT_ENTRY_STATE_ARG, PDFS_GET_PKT_ENTRY_STATE_ARG structure pointer [Distributed File System], dfs.dfs_get_pkt_entry_state_arg, lmdfs/DFS_GET_PKT_ENTRY_STATE_ARG, lmdfs/PDFS_GET_PKT_ENTRY_STATE_ARG'
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: DFS_GET_PKT_ENTRY_STATE_ARG, *PDFS_GET_PKT_ENTRY_STATE_ARG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDFS_GET_PKT_ENTRY_STATE_ARG
 - lmdfs/PDFS_GET_PKT_ENTRY_STATE_ARG
 - DFS_GET_PKT_ENTRY_STATE_ARG
 - lmdfs/DFS_GET_PKT_ENTRY_STATE_ARG
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
 - DFS_GET_PKT_ENTRY_STATE_ARG
---

# DFS_GET_PKT_ENTRY_STATE_ARG structure


## -description

Input buffer used with the 
    <a href="/windows/desktop/dfs/fsctl-dfs-get-pkt-entry-state">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
    code.

## -struct-fields

### -field DfsEntryPathLen

Length of the DFS Entry Path Unicode string in bytes stored in the <i>Buffer</i> 
      parameter.

### -field ServerNameLen

Length of the Server Name Unicode string in bytes stored in the <i>Buffer</i> parameter 
      following the DFS Entry Path string.

### -field ShareNameLen

Length of the Share Name Unicode string in bytes stored in the <i>Buffer</i> parameter 
      following the Server Name string.

### -field Level

Length of the Level string in bytes.



#### 1

Return the DFS root or DFS link name. On return the output buffer for the 
        <a href="/windows/desktop/dfs/fsctl-dfs-get-pkt-entry-state">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
        code contains a <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1">DFS_INFO_1</a> structure.



#### 2

Return the DFS root or DFS link name, status, and the number of DFS targets. On return the output buffer 
        for the <a href="/windows/desktop/dfs/fsctl-dfs-get-pkt-entry-state">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> 
        control code contains a <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2">DFS_INFO_2</a> structure.



#### 3

Return the DFS root or DFS link name, status, and  target information. On return output buffer for the 
        <a href="/windows/desktop/dfs/fsctl-dfs-get-pkt-entry-state">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
        code contains a <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3">DFS_INFO_3</a> structure.



#### 4

Return the DFS root or DFS link name, status, <b>GUID</b>, time-out, and target 
        information. On return the output buffer for the 
        <a href="/windows/desktop/dfs/fsctl-dfs-get-pkt-entry-state">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
        code contains a <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4">DFS_INFO_4</a> structure.



#### 101

Set the storage state associated with the DFS root or link specified in the DFS Entry Path string. On the 
        return output buffer for the 
        <a href="/windows/desktop/dfs/fsctl-dfs-get-pkt-entry-state">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
        code contains a <a href="/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101">DFS_INFO_101</a> structure.

### -field Buffer

On input this contains the three Unicode strings in order. The Unicode strings are not 
      <b>NULL</b> terminated and there is no delimiter between the strings.

## -see-also

<a href="/previous-versions/windows/desktop/dfs/distributed-file-system-structures">Distributed File System Structures</a>



<a href="/windows/desktop/dfs/fsctl-dfs-get-pkt-entry-state">FSCTL_DFS_GET_PKT_ENTRY_STATE</a>



<a href="/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo">NetDfsGetClientInfo</a>

