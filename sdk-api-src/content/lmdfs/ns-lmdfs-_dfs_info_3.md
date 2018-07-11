---
UID: NS:lmdfs._DFS_INFO_3
title: "_DFS_INFO_3"
author: windows-sdk-content
description: Contains information about a Distributed File System (DFS) root or link. This structure contains the name, status, number of DFS targets, and information about each target of the root or link.
old-location: dfs\dfs_info_3_str.htm
old-project: dfs
ms.assetid: fd60cb52-fa17-4cac-a7e8-9803303336dc
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: "*LPDFS_INFO_3, *PDFS_INFO_3, DFS_INFO_3, DFS_INFO_3 structure [Distributed File System], DFS_VOLUME_FLAVOR_AD_BLOB, DFS_VOLUME_FLAVOR_STANDALONE, DFS_VOLUME_STATE_INCONSISTENT, DFS_VOLUME_STATE_OFFLINE, DFS_VOLUME_STATE_OK, DFS_VOLUME_STATE_ONLINE, LPDFS_INFO_3, LPDFS_INFO_3 structure pointer [Distributed File System], PDFS_INFO_3, PDFS_INFO_3 structure pointer [Distributed File System], _DFS_INFO_3, _win32_dfs_info_3_str, dfs.dfs_info_3_str, fs.dfs_info_3_str, lmdfs/DFS_INFO_3, lmdfs/LPDFS_INFO_3, lmdfs/PDFS_INFO_3, netmgmt.dfs_info_3_str"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DFS_INFO_3, *PDFS_INFO_3, *LPDFS_INFO_3
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LmDfs.h
api_name:
 - DFS_INFO_3
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _DFS_INFO_3 structure


## -description


Contains information about a Distributed File System (DFS) root or link. This structure contains the name, 
    status, number of DFS targets, and information about each target of the root or link. This structure is only for 
    use with the <a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>, 
    <a href="https://msdn.microsoft.com/065ec002-cb90-4d78-a70c-6ac37f71994f">NetDfsGetClientInfo</a>, and 
    <a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a> functions and the 
    <a href="https://msdn.microsoft.com/d4eec104-128b-43b5-9fae-08ab0b977dec">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
    code.


## -struct-fields




### -field EntryPath

Pointer to a null-terminated Unicode string that specifies the Universal Naming Convention (UNC) path of a 
       DFS root or link.

For a link, the string can be in one of two forms. The first form is as follows:

\\<i>ServerName</i>\<i>DfsName</i>\<i>link_path</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone 
       DFS namespace; <i>DfsName</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

The second form is as follows:

\\<i>DomainName</i>\<i>DomDfsname</i>\<i>link_path</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS 
       namespace; <i>DomDfsname</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

For a root, the string can be in one of two forms:

\\<i>ServerName</i>\<i>DfsName</i>

or

\\<i>DomainName</i>\<i>DomDfsname</i>

where the values of the names are the same as those described previously.


### -field Comment

Pointer to a null-terminated Unicode string that contains a comment associated with the DFS root or 
      link.


### -field State

Specifies a set of bit flags that describe the DFS root or link. One 
      <b>DFS_VOLUME_STATE</b> flag is set, and one <b>DFS_VOLUME_FLAVOR</b> flag 
      is set. The <b>DFS_VOLUME_FLAVORS</b> bitmask (0x00000300) must be used to extract the DFS 
      namespace flavor, and the <b>DFS_VOLUME_STATES</b> bitmask (0x0000000F) must be used to 
      extract the DFS root or link state from this member. For an example that describes the interpretation of the 
      flags, see the Remarks section of <a href="https://msdn.microsoft.com/c5fe27be-fd6e-4cf0-abf6-8363c78edf5b">DFS_INFO_2</a>.



#### DFS_VOLUME_STATE_OK (0x00000001)

The specified DFS root or link is in the normal state.



#### DFS_VOLUME_STATE_INCONSISTENT (0x00000002)

The internal DFS database is inconsistent with the specified DFS root or link. Attempts to repair the 
        inconsistency have failed.



#### DFS_VOLUME_STATE_OFFLINE (0x00000003)

The specified DFS root or link is offline or unavailable.



#### DFS_VOLUME_STATE_ONLINE (0x00000004)

The specified DFS root or link is available.



#### DFS_VOLUME_FLAVOR_STANDALONE (0x00000100)

The system sets this flag if the root is associated with a stand-alone DFS namespace.



#### DFS_VOLUME_FLAVOR_AD_BLOB (0x00000200)

The system sets this flag if the root is associated with a domain-based DFS namespace.


### -field NumberOfStorages

Specifies the number of DFS targets.


### -field Storage.size_is

 


### -field Storage.size_is.NumberOfStorages

 


### -field Storage

Pointer to an array of <a href="https://msdn.microsoft.com/f50f32d8-1745-4ff6-97a6-ddd6fff95955">DFS_STORAGE_INFO</a> 
      structures. The <b>NumberOfStorages</b> member specifies the number of structures in the 
      array.


## -remarks



A <b>DFS_INFO_3</b> structure contains one or more 
    <a href="https://msdn.microsoft.com/f50f32d8-1745-4ff6-97a6-ddd6fff95955">DFS_STORAGE_INFO</a> structures, one for each DFS 
    target.




## -see-also




<a href="https://msdn.microsoft.com/f50f32d8-1745-4ff6-97a6-ddd6fff95955">DFS_STORAGE_INFO</a>



<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>



<a href="https://msdn.microsoft.com/065ec002-cb90-4d78-a70c-6ac37f71994f">NetDfsGetClientInfo</a>



<a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>
 

 

