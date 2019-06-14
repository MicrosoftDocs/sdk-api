---
UID: NS:lmdfs._DFS_INFO_150
title: DFS_INFO_150 (lmdfs.h)
author: windows-sdk-content
description: Contains the security descriptor for a DFS link's reparse point.
old-location: dfs\dfs_info_150.htm
tech.root: Dfs
ms.assetid: b0fa6fca-8e60-447d-9334-c4df04f13439
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDFS_INFO_150, *PDFS_INFO_150, DFS_INFO_150, DFS_INFO_150 structure [Distributed File System], PDFS_INFO_150, PDFS_INFO_150 structure pointer [Distributed File System], dfs.dfs_info_150, fs.dfs_info_150, lmdfs/DFS_INFO_150, lmdfs/PDFS_INFO_150"
ms.topic: struct
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
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
 - DFS_INFO_150
product: Windows
targetos: Windows
req.typenames: DFS_INFO_150, *PDFS_INFO_150, *LPDFS_INFO_150
req.redist: 
ms.custom: 19H1
---

# DFS_INFO_150 structure


## -description


Contains the security descriptor for a DFS link's reparse point. This structure is only for 
     use with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a> and 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo">NetDfsSetInfo</a> functions.


## -struct-fields




### -field SecurityDescriptorLength

 


### -field pSecurityDescriptor.size_is

 


### -field pSecurityDescriptor.size_is.SecurityDescriptorLength

 


### -field SdLengthReserved

This member is reserved for system use.


### -field pSecurityDescriptor

Pointer to a  <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_security_descriptor">SECURITY_DESCRIPTOR</a> 
      structure that specifies a self-relative security descriptor to be associated with the DFS link's reparse 
      point. This field is valid for DFS links only.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo">NetDfsSetInfo</a>
 

 

