---
UID: NS:lmdfs._DFS_INFO_4
title: DFS_INFO_4 (lmdfs.h)
description: Contains information about a Distributed File System (DFS) root or link. This structure contains the name, status, GUID, time-out, number of targets, and information about each target of the root or link.helpviewer_keywords: ["*LPDFS_INFO_4","*PDFS_INFO_4","DFS_INFO_4","DFS_INFO_4 structure [Distributed File System]","DFS_VOLUME_FLAVOR_AD_BLOB","DFS_VOLUME_FLAVOR_STANDALONE","DFS_VOLUME_STATE_INCONSISTENT","DFS_VOLUME_STATE_OFFLINE","DFS_VOLUME_STATE_OK","DFS_VOLUME_STATE_ONLINE","LPDFS_INFO_4","LPDFS_INFO_4 structure pointer [Distributed File System]","PDFS_INFO_4","PDFS_INFO_4 structure pointer [Distributed File System]","_win32_dfs_info_4_str","dfs.dfs_info_4_str","fs.dfs_info_4_str","lmdfs/DFS_INFO_4","lmdfs/LPDFS_INFO_4","lmdfs/PDFS_INFO_4","netmgmt.dfs_info_4_str"]
old-location: dfs\dfs_info_4_str.htm
tech.root: Dfs
ms.assetid: 0b255be8-b719-4f40-9051-7e8a1bffa0e0
ms.date: 12/05/2018
ms.keywords: '*LPDFS_INFO_4, *PDFS_INFO_4, DFS_INFO_4, DFS_INFO_4 structure [Distributed File System], DFS_VOLUME_FLAVOR_AD_BLOB, DFS_VOLUME_FLAVOR_STANDALONE, DFS_VOLUME_STATE_INCONSISTENT, DFS_VOLUME_STATE_OFFLINE, DFS_VOLUME_STATE_OK, DFS_VOLUME_STATE_ONLINE, LPDFS_INFO_4, LPDFS_INFO_4 structure pointer [Distributed File System], PDFS_INFO_4, PDFS_INFO_4 structure pointer [Distributed File System], _win32_dfs_info_4_str, dfs.dfs_info_4_str, fs.dfs_info_4_str, lmdfs/DFS_INFO_4, lmdfs/LPDFS_INFO_4, lmdfs/PDFS_INFO_4, netmgmt.dfs_info_4_str'
f1_keywords:
- lmdfs/DFS_INFO_4
dev_langs:
- c++
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
- DFS_INFO_4
targetos: Windows
req.typenames: DFS_INFO_4, *PDFS_INFO_4, *LPDFS_INFO_4
req.redist: 
ms.custom: 19H1
---

# DFS_INFO_4 structure


## -description


Contains information about a Distributed File System (DFS) root or link. This structure contains the 
    name, status, <b>GUID</b>, time-out, number of targets, and information about each target of 
    the root or link. This structure is only for use with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum">NetDfsEnum</a>, 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo">NetDfsGetClientInfo</a>, and 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a> functions and the 
    <a href="https://docs.microsoft.com/windows/desktop/dfs/fsctl-dfs-get-pkt-entry-state">FSCTL_DFS_GET_PKT_ENTRY_STATE</a> control 
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
      extract the DFS root or link state from this field. For an example that describes the interpretation of the 
      flags, see the Remarks section of <a href="https://docs.microsoft.com/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2">DFS_INFO_2</a>.



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


### -field Timeout

Specifies the time-out, in seconds, of the DFS root or link.


### -field Guid

Specifies the GUID of the DFS root or link.


### -field NumberOfStorages

Specifies the number of DFS targets.


### -field Storage.size_is

 


### -field Storage.size_is.NumberOfStorages

 


### -field Storage

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info">DFS_STORAGE_INFO</a> 
      structures. The <b>NumberOfStorages</b> member specifies the number of structures in the 
      array.


## -remarks



A <b>DFS_INFO_4</b> structure contains one or more 
    <a href="https://docs.microsoft.com/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info">DFS_STORAGE_INFO</a> structures, one for each DFS 
    target.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info">DFS_STORAGE_INFO</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions">Distributed File System (DFS) Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum">NetDfsEnum</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo">NetDfsGetClientInfo</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo">NetDfsGetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>
 

 

