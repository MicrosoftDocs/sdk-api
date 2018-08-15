---
UID: NS:lmdfs._DFS_INFO_150
title: "_DFS_INFO_150"
author: windows-sdk-content
description: Contains the security descriptor for a DFS link's reparse point.
old-location: dfs\dfs_info_150.htm
old-project: dfs
ms.assetid: b0fa6fca-8e60-447d-9334-c4df04f13439
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPDFS_INFO_150, *PDFS_INFO_150, DFS_INFO_150, DFS_INFO_150 structure [Distributed File System], PDFS_INFO_150, PDFS_INFO_150 structure pointer [Distributed File System], _DFS_INFO_150, dfs.dfs_info_150, fs.dfs_info_150, lmdfs/DFS_INFO_150, lmdfs/PDFS_INFO_150"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.redist: 
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
tech.root: 
req.typenames: DFS_INFO_150, *PDFS_INFO_150, *LPDFS_INFO_150
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DFS_INFO_150 structure


## -description


Contains the security descriptor for a DFS link's reparse point. This structure is only for 
     use with the <a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a> and 
     <a href="https://msdn.microsoft.com/5526afa7-82bc-47c7-99d6-44e41ef772b1">NetDfsSetInfo</a> functions.


## -struct-fields




### -field SecurityDescriptorLength

 


### -field pSecurityDescriptor.size_is

 


### -field pSecurityDescriptor.size_is.SecurityDescriptorLength

 


### -field SdLengthReserved

This member is reserved for system use.


### -field pSecurityDescriptor

Pointer to a  <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> 
      structure that specifies a self-relative security descriptor to be associated with the DFS link's reparse 
      point. This field is valid for DFS links only.


## -see-also




<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System Functions</a>



<a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a>



<a href="https://msdn.microsoft.com/5526afa7-82bc-47c7-99d6-44e41ef772b1">NetDfsSetInfo</a>
 

 

