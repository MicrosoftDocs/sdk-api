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
 

 

