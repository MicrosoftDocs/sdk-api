---
UID: NS:clfs._CLS_CONTAINER_INFORMATION
title: CLS_CONTAINER_INFORMATION (clfs.h)
description: Describes general information about a container.
helpviewer_keywords: ["*PCLFS_CONTAINER_INFORMATION","*PCLS_CONTAINER_INFORMATION","CLFS_CONTAINER_INFORMATION","CLFS_CONTAINER_INFORMATION structure [Files]","CLS_CONTAINER_INFORMATION","ClfsContainerActive","ClfsContainerActivePendingDelete","ClfsContainerInactive","ClfsContainerInitializing","ClfsContainerPendingArchive","ClfsContainerPendingArchiveAndDelete","PCLFS_CONTAINER_INFORMATION","PCLFS_CONTAINER_INFORMATION structure pointer [Files]","PPCLFS_CONTAINER_INFORMATION","PPCLFS_CONTAINER_INFORMATION structure pointer [Files]","PPCLS_CONTAINER_INFORMATION","clfs/PCLFS_CONTAINER_INFORMATION","clfs/PPCLFS_CONTAINER_INFORMATION","clfs/_CLFS_CONTAINER_INFORMATION","fs.clfs_container_information"]
old-location: fs\clfs_container_information.htm
tech.root: fs
ms.assetid: 3788fac0-4e99-49e0-bba1-6a6d22299950
ms.date: 12/05/2018
ms.keywords: '*PCLFS_CONTAINER_INFORMATION, *PCLS_CONTAINER_INFORMATION, CLFS_CONTAINER_INFORMATION, CLFS_CONTAINER_INFORMATION structure [Files], CLS_CONTAINER_INFORMATION, ClfsContainerActive, ClfsContainerActivePendingDelete, ClfsContainerInactive, ClfsContainerInitializing, ClfsContainerPendingArchive, ClfsContainerPendingArchiveAndDelete, PCLFS_CONTAINER_INFORMATION, PCLFS_CONTAINER_INFORMATION structure pointer [Files], PPCLFS_CONTAINER_INFORMATION, PPCLFS_CONTAINER_INFORMATION structure pointer [Files], PPCLS_CONTAINER_INFORMATION, clfs/PCLFS_CONTAINER_INFORMATION, clfs/PPCLFS_CONTAINER_INFORMATION, clfs/_CLFS_CONTAINER_INFORMATION, fs.clfs_container_information'
req.header: clfs.h
req.include-header: Clfsw32.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: CLS_CONTAINER_INFORMATION, *PCLS_CONTAINER_INFORMATION, PPCLS_CONTAINER_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLS_CONTAINER_INFORMATION
 - clfs/_CLS_CONTAINER_INFORMATION
 - PCLS_CONTAINER_INFORMATION
 - clfs/PCLS_CONTAINER_INFORMATION
 - CLS_CONTAINER_INFORMATION
 - clfs/CLS_CONTAINER_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Clfs.h
api_name:
 - CLFS_CONTAINER_INFORMATION
---

# CLS_CONTAINER_INFORMATION structure


## -description

Describes general information about a container.  The <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogcontainerscancontext">CreateLogContainerScanContext</a> and <a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a> functions use container descriptors to scan and return information  about all  Common Log File System (CLFS) containers.

## -struct-fields

### -field FileAttributes

The file system attributes. CLFS uses the following attributes:

<ul>
<li>FILE_ATTRIBUTE_ARCHIVE - The log is not ephemeral.
</li>
<li>FILE_ATTRIBUTE_DEDICATED - The log is not multiplexed.
</li>
<li>FILE_ATTRIBUTE_READONLY - The file is read-only. Applications can read the file, but cannot write to it or delete it.</li>
</ul>
CLFS ignores but preserves all other file attribute values. The <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa">SetFileAttributes</a> topic lists the valid values for attributes.

### -field CreationTime

The time a file is created.

### -field LastAccessTime

The last time a container is read from or written to.

### -field LastWriteTime

The last time a container is written to.

### -field ContainerSize

The size of a container, in bytes.

### -field FileNameActualLength

The size of the actual file name, in characters. 

This number is  different than  <b>FileNameLength</b>  when the file name of the container  is longer than MAX_PATH_LENGTH.

### -field FileNameLength

The size of the file name in the <i>FileName</i> buffer, in characters.

### -field FileName

A pointer to a string that contains the file name for a container.

### -field State

The current state of a container.  

This member can be one of the  following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ClfsContainerInitializing"></a><a id="clfscontainerinitializing"></a><a id="CLFSCONTAINERINITIALIZING"></a><dl>
<dt><b>ClfsContainerInitializing</b></dt>
</dl>
</td>
<td width="60%">
The container is in the process of initializing.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsContainerInactive"></a><a id="clfscontainerinactive"></a><a id="CLFSCONTAINERINACTIVE"></a><dl>
<dt><b>ClfsContainerInactive</b></dt>
</dl>
</td>
<td width="60%">
The container  is allocated, but  is not in the active region of the log. 

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsContainerActive"></a><a id="clfscontaineractive"></a><a id="CLFSCONTAINERACTIVE"></a><dl>
<dt><b>ClfsContainerActive</b></dt>
</dl>
</td>
<td width="60%">
The container is being used as storage for part of the  log.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsContainerActivePendingDelete"></a><a id="clfscontaineractivependingdelete"></a><a id="CLFSCONTAINERACTIVEPENDINGDELETE"></a><dl>
<dt><b>ClfsContainerActivePendingDelete</b></dt>
</dl>
</td>
<td width="60%">
The container is marked for deletion, but still contains part of the active log.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsContainerPendingArchive"></a><a id="clfscontainerpendingarchive"></a><a id="CLFSCONTAINERPENDINGARCHIVE"></a><dl>
<dt><b>ClfsContainerPendingArchive</b></dt>
</dl>
</td>
<td width="60%">
The container is marked for archive.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsContainerPendingArchiveAndDelete"></a><a id="clfscontainerpendingarchiveanddelete"></a><a id="CLFSCONTAINERPENDINGARCHIVEANDDELETE"></a><dl>
<dt><b>ClfsContainerPendingArchiveAndDelete</b></dt>
</dl>
</td>
<td width="60%">
The container is marked for deletion, but still contains log data that is not  archived.

</td>
</tr>
</table>

### -field PhysicalContainerId

The physical container identifier that  cannot  be changed.

### -field LogicalContainerId

The logical container identifier that  changes every time the container is recycled.

## -see-also

<a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogcontainerscancontext">CreateLogContainerScanContext</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-getlogcontainername">GetLogContainerName</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-scanlogcontainers">ScanLogContainers</a>