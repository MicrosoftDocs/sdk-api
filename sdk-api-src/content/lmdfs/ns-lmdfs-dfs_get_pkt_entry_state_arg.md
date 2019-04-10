---
UID: NS:lmdfs.__unnamed_struct_2
title: DFS_GET_PKT_ENTRY_STATE_ARG (lmdfs.h)
author: windows-sdk-content
description: Input buffer used with the FSCTL_DFS_GET_PKT_ENTRY_STATE control code.
old-location: dfs\dfs_get_pkt_entry_state_arg.htm
tech.root: Dfs
ms.assetid: eb69d346-d88c-48e8-abd7-5cbb5976f41f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDFS_GET_PKT_ENTRY_STATE_ARG, DFS_GET_PKT_ENTRY_STATE_ARG, DFS_GET_PKT_ENTRY_STATE_ARG structure [Distributed File System], PDFS_GET_PKT_ENTRY_STATE_ARG, PDFS_GET_PKT_ENTRY_STATE_ARG structure pointer [Distributed File System], dfs.dfs_get_pkt_entry_state_arg, lmdfs/DFS_GET_PKT_ENTRY_STATE_ARG, lmdfs/PDFS_GET_PKT_ENTRY_STATE_ARG"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LmDfs.h
api_name:
 - DFS_GET_PKT_ENTRY_STATE_ARG
product: Windows
targetos: Windows
req.typenames: DFS_GET_PKT_ENTRY_STATE_ARG, *PDFS_GET_PKT_ENTRY_STATE_ARG
req.redist: 
---

# DFS_GET_PKT_ENTRY_STATE_ARG structure


## -description


Input buffer used with the 
    <a href="https://msdn.microsoft.com/d4eec104-128b-43b5-9fae-08ab0b977dec">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
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
        <a href="https://msdn.microsoft.com/d4eec104-128b-43b5-9fae-08ab0b977dec">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
        code contains a <a href="https://msdn.microsoft.com/96647570-badd-4925-ab90-054a00ba04c4">DFS_INFO_1</a> structure.



#### 2

Return the DFS root or DFS link name, status, and the number of DFS targets. On return the output buffer 
        for the <a href="https://msdn.microsoft.com/d4eec104-128b-43b5-9fae-08ab0b977dec">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> 
        control code contains a <a href="https://msdn.microsoft.com/c5fe27be-fd6e-4cf0-abf6-8363c78edf5b">DFS_INFO_2</a> structure.



#### 3

Return the DFS root or DFS link name, status, and  target information. On return output buffer for the 
        <a href="https://msdn.microsoft.com/d4eec104-128b-43b5-9fae-08ab0b977dec">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
        code contains a <a href="https://msdn.microsoft.com/fd60cb52-fa17-4cac-a7e8-9803303336dc">DFS_INFO_3</a> structure.



#### 4

Return the DFS root or DFS link name, status, <b>GUID</b>, time-out, and target 
        information. On return the output buffer for the 
        <a href="https://msdn.microsoft.com/d4eec104-128b-43b5-9fae-08ab0b977dec">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
        code contains a <a href="https://msdn.microsoft.com/0b255be8-b719-4f40-9051-7e8a1bffa0e0">DFS_INFO_4</a> structure.



#### 101

Set the storage state associated with the DFS root or link specified in the DFS Entry Path string. On the 
        return output buffer for the 
        <a href="https://msdn.microsoft.com/d4eec104-128b-43b5-9fae-08ab0b977dec">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
        code contains a <a href="https://msdn.microsoft.com/506aaf68-2f23-4dd2-b43c-aeb86334a3d8">DFS_INFO_101</a> structure.


### -field Buffer

On input this contains the three Unicode strings in order. The Unicode strings are not 
      <b>NULL</b> terminated and there is no delimiter between the strings.


## -see-also




<a href="https://msdn.microsoft.com/f55ad3c0-0457-4d5a-a7d3-8eff744d573d">Distributed File System Structures</a>



<a href="https://msdn.microsoft.com/d4eec104-128b-43b5-9fae-08ab0b977dec">FSCTL_DFS_GET_PKT_ENTRY_STATE</a>



<a href="https://msdn.microsoft.com/065ec002-cb90-4d78-a70c-6ac37f71994f">NetDfsGetClientInfo</a>
 

 

