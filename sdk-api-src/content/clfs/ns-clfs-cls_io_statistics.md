---
UID: NS:clfs._CLS_IO_STATISTICS
title: CLS_IO_STATISTICS (clfs.h)
author: windows-sdk-content
description: Defines the statistics that are reported by GetLogIoStatistics.
old-location: fs\clfs_io_statistics.htm
tech.root: Clfs
ms.assetid: 99544331-0a7c-4efd-93a7-e94011375394
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PCLFS_IO_STATISTICS, *PCLS_IO_STATISTICS, CLFS_IO_STATISTICS, CLFS_IO_STATISTICS structure [Files], CLS_IO_STATISTICS, PCLFS_IO_STATISTICS, PCLFS_IO_STATISTICS structure pointer [Files], PPCLFS_IO_STATISTICS, PPCLFS_IO_STATISTICS structure pointer [Files], PPCLS_IO_STATISTICS, clfs/PCLFS_IO_STATISTICS, clfs/PPCLFS_IO_STATISTICS, clfs/_CLFS_IO_STATISTICS, fs.clfs_io_statistics'
ms.topic: struct
f1_keywords:
- clfs/CLFS_IO_STATISTICS
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Clfs.h
api_name:
- CLFS_IO_STATISTICS
targetos: Windows
req.typenames: CLS_IO_STATISTICS, *PCLS_IO_STATISTICS, PPCLS_IO_STATISTICS
req.redist: 
ms.custom: 19H1
---

# CLS_IO_STATISTICS structure


## -description


Defines the  statistics that are reported by  <a href="https://docs.microsoft.com/windows/desktop/api/clfsw32/nf-clfsw32-getlogiostatistics">GetLogIoStatistics</a>.  Initially, statistics packets report only flush statistics, including the frequency of data and metadata flushes on a physical log and the amount of data and metadata flushed.  The flush statistics are defined by the following I/O statistics packet types.


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




<a href="https://docs.microsoft.com/windows/desktop/api/clfs/ns-clfs-cls_io_statistics_header">CLFS_IO_STATISTICS_HEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clfsw32/nf-clfsw32-getlogiostatistics">GetLogIoStatistics</a>
 

 

