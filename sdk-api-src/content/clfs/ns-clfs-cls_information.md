---
UID: NS:clfs._CLS_INFORMATION
title: CLS_INFORMATION (clfs.h)
description: Describes general information about a log.
helpviewer_keywords: ["*PCLFS_INFORMATION","*PCLS_INFORMATION","*PPCLS_INFORMATION","CLFS_INFORMATION","CLFS_INFORMATION structure [Files]","CLS_INFORMATION","PCLFS_INFORMATION","PCLFS_INFORMATION structure pointer [Files]","PPCLFS_INFORMATION","PPCLFS_INFORMATION structure pointer [Files]","clfs/PCLFS_INFORMATION","clfs/PPCLFS_INFORMATION","clfs/_CLFS_INFORMATION","fs.clfs_information"]
old-location: fs\clfs_information.htm
tech.root: fs
ms.assetid: 06f5919e-b98f-4502-9653-9ef42c1ebe5a
ms.date: 12/05/2018
ms.keywords: '*PCLFS_INFORMATION, *PCLS_INFORMATION, *PPCLS_INFORMATION, CLFS_INFORMATION, CLFS_INFORMATION structure [Files], CLS_INFORMATION, PCLFS_INFORMATION, PCLFS_INFORMATION structure pointer [Files], PPCLFS_INFORMATION, PPCLFS_INFORMATION structure pointer [Files], clfs/PCLFS_INFORMATION, clfs/PPCLFS_INFORMATION, clfs/_CLFS_INFORMATION, fs.clfs_information'
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
req.typenames: CLS_INFORMATION, *PCLS_INFORMATION, *PPCLS_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLS_INFORMATION
 - clfs/_CLS_INFORMATION
 - PCLS_INFORMATION
 - clfs/PCLS_INFORMATION
 - CLS_INFORMATION
 - clfs/CLS_INFORMATION
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
 - CLFS_INFORMATION
---

# CLS_INFORMATION structure


## -description

Describes general information about a log. The <a href="/windows/desktop/api/clfsw32/nf-clfsw32-getlogfileinformation">GetLogFileInformation</a> function returns the <b>CLFS_INFORMATION</b> structure.

## -struct-fields

### -field TotalAvailable

The total available space that is allocated to a log, in bytes.  

This member is the sum of the sizes of all containers that are allocated to the dedicated log.

### -field CurrentAvailable

The space that is available in a log to  append new records and reservation allocations, in bytes.

### -field TotalReservation

The total space in a  log that is dedicated to reservation allocations.

### -field BaseFileSize

The size of the base log, in bytes.

### -field ContainerSize

The size of a container, in bytes.

### -field TotalContainers

The number of active containers that are associated with a dedicated log.

### -field FreeContainers

The number of containers that are not in an active log.

### -field TotalClients

The number of  log streams  that are active in a physical log.

### -field Attributes

The log  attributes that are set by using the <i>fFlagsAndAttributes</i> parameter of <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a> when a log is created.

### -field FlushThreshold

The number of bytes of data that can remain pending on the internal flush queue before  the Common Log File System (CLFS)  automatically writes the data to disk.

### -field SectorSize

The sector size of the underlying disk geometry, in bytes.  

The sector size is assumed to be a multiple of 512 and consistent across log containers.

### -field MinArchiveTailLsn

The log sequence number (LSN) of the log archive tail.

### -field BaseLsn

The LSN that marks the start of the active region of a log.

### -field LastFlushedLsn

The value of <b>LastFlushedLsn</b> indicates that any LSNs smaller than the one specified are already  flushed to disk.

### -field LastLsn

The value of <b>LastLsn</b> indicates that any LSNs smaller than the one specified are already  appended to the log.

### -field RestartLsn

The LSN of the last written restart record.  

If the log  does not have a  restart area, the LSN has the value of CLFS_LSN_INVALID.

### -field Identity

The unique identifier for a log.

## -see-also

<a href="/windows/desktop/api/clfsw32/nf-clfsw32-getlogfileinformation">GetLogFileInformation</a>