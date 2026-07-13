---
UID: NE:clfs._CLFS_IOSTATS_CLASS
title: CLFS_IOSTATS_CLASS (clfs.h)
description: Defines types of I/O statistics reported by CLFS and is used when a client calls GetLogIoStatistics.
helpviewer_keywords: ["*PCLFS_IOSTATS_CLASS","CLFS_IOSTATS_CLASS","CLFS_IOSTATS_CLASS enumeration [Files]","ClfsIoStatsDefault","ClfsIoStatsMax","PCLFS_IOSTATS_CLASS","PCLFS_IOSTATS_CLASS enumeration pointer [Files]","PPCLFS_IOSTATS_CLASS","PPCLFS_IOSTATS_CLASS enumeration pointer [Files]","clfs/CLFS_IOSTATS_CLASS","clfs/ClfsIoStatsDefault","clfs/ClfsIoStatsMax","clfs/PCLFS_IOSTATS_CLASS","clfs/PPCLFS_IOSTATS_CLASS","fs.clfs_iostats_class"]
old-location: fs\clfs_iostats_class.htm
tech.root: fs
ms.assetid: 8ba1f5e4-9af3-4c8a-8b57-b6075d0560d6
ms.date: 12/05/2018
ms.keywords: '*PCLFS_IOSTATS_CLASS, CLFS_IOSTATS_CLASS, CLFS_IOSTATS_CLASS enumeration [Files], ClfsIoStatsDefault, ClfsIoStatsMax, PCLFS_IOSTATS_CLASS, PCLFS_IOSTATS_CLASS enumeration pointer [Files], PPCLFS_IOSTATS_CLASS, PPCLFS_IOSTATS_CLASS enumeration pointer [Files], clfs/CLFS_IOSTATS_CLASS, clfs/ClfsIoStatsDefault, clfs/ClfsIoStatsMax, clfs/PCLFS_IOSTATS_CLASS, clfs/PPCLFS_IOSTATS_CLASS, fs.clfs_iostats_class'
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
req.typenames: CLFS_IOSTATS_CLASS, *PCLFS_IOSTATS_CLASS, PPCLFS_IOSTATS_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLFS_IOSTATS_CLASS
 - clfs/_CLFS_IOSTATS_CLASS
 - PCLFS_IOSTATS_CLASS
 - clfs/PCLFS_IOSTATS_CLASS
 - CLFS_IOSTATS_CLASS
 - clfs/CLFS_IOSTATS_CLASS
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
 - CLFS_IOSTATS_CLASS
---

# CLFS_IOSTATS_CLASS enumeration


## -description

Defines types of I/O statistics reported by CLFS and is used when a client calls <a href="/windows/desktop/api/clfsw32/nf-clfsw32-getlogiostatistics">GetLogIoStatistics</a>.  Currently, log flush rates are the only type of statistic reported, but this enumeration will reflect more types of statistics in the future.

## -enum-fields

### -field ClfsIoStatsDefault:0x0000

The default I/O statistics exported.

### -field ClfsIoStatsMax:0xFFFF

The log flush rate.

## -see-also

<a href="/windows/desktop/api/clfsw32/nf-clfsw32-getlogiostatistics">GetLogIoStatistics</a>
