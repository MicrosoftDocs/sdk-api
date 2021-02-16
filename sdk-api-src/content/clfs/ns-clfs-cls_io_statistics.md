---
UID: NS:clfs._CLS_IO_STATISTICS
title: CLS_IO_STATISTICS (clfs.h)
description: Defines the statistics that are reported by GetLogIoStatistics.
helpviewer_keywords: ["*PCLFS_IO_STATISTICS","*PCLS_IO_STATISTICS","CLFS_IO_STATISTICS","CLFS_IO_STATISTICS structure [Files]","CLS_IO_STATISTICS","PCLFS_IO_STATISTICS","PCLFS_IO_STATISTICS structure pointer [Files]","PPCLFS_IO_STATISTICS","PPCLFS_IO_STATISTICS structure pointer [Files]","PPCLS_IO_STATISTICS","clfs/PCLFS_IO_STATISTICS","clfs/PPCLFS_IO_STATISTICS","clfs/_CLFS_IO_STATISTICS","fs.clfs_io_statistics"]
old-location: fs\clfs_io_statistics.htm
tech.root: fs
ms.assetid: 99544331-0a7c-4efd-93a7-e94011375394
ms.date: 12/05/2018
ms.keywords: '*PCLFS_IO_STATISTICS, *PCLS_IO_STATISTICS, CLFS_IO_STATISTICS, CLFS_IO_STATISTICS structure [Files], CLS_IO_STATISTICS, PCLFS_IO_STATISTICS, PCLFS_IO_STATISTICS structure pointer [Files], PPCLFS_IO_STATISTICS, PPCLFS_IO_STATISTICS structure pointer [Files], PPCLS_IO_STATISTICS, clfs/PCLFS_IO_STATISTICS, clfs/PPCLFS_IO_STATISTICS, clfs/_CLFS_IO_STATISTICS, fs.clfs_io_statistics'
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
req.typenames: CLS_IO_STATISTICS, *PCLS_IO_STATISTICS, PPCLS_IO_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLS_IO_STATISTICS
 - clfs/_CLS_IO_STATISTICS
 - PCLS_IO_STATISTICS
 - clfs/PCLS_IO_STATISTICS
 - CLS_IO_STATISTICS
 - clfs/CLS_IO_STATISTICS
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
 - CLFS_IO_STATISTICS
---

# CLS_IO_STATISTICS structure


## -description

Defines the  statistics that are reported by  <a href="/windows/desktop/api/clfsw32/nf-clfsw32-getlogiostatistics">GetLogIoStatistics</a>.  Initially, statistics packets report only flush statistics, including the frequency of data and metadata flushes on a physical log and the amount of data and metadata flushed.  The flush statistics are defined by the following I/O statistics packet types.

## -struct-fields

### -field hdrIoStats

The header for the statistics buffer.

### -field cFlush

The frequency of  data flushes  for the logging session.

### -field cbFlush

The cumulative number of bytes of data  flushed in the logging session.

### -field cMetaFlush

The frequency of  metadata flushes  for the logging session.

### -field cbMetaFlush

The cumulative number of bytes of metadata flushed in the logging session.

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_io_statistics_header">CLFS_IO_STATISTICS_HEADER</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-getlogiostatistics">GetLogIoStatistics</a>