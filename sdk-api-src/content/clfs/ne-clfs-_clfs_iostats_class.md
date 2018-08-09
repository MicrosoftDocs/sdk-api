---
UID: NE:clfs._CLFS_IOSTATS_CLASS
title: "_CLFS_IOSTATS_CLASS"
author: windows-sdk-content
description: Defines types of I/O statistics reported by CLFS and is used when a client calls GetLogIoStatistics.
old-location: fs\clfs_iostats_class.htm
old-project: Clfs
ms.assetid: 8ba1f5e4-9af3-4c8a-8b57-b6075d0560d6
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: "*PCLFS_IOSTATS_CLASS, CLFS_IOSTATS_CLASS, CLFS_IOSTATS_CLASS enumeration [Files], ClfsIoStatsDefault, ClfsIoStatsMax, PCLFS_IOSTATS_CLASS, PCLFS_IOSTATS_CLASS enumeration pointer [Files], PPCLFS_IOSTATS_CLASS, PPCLFS_IOSTATS_CLASS enumeration pointer [Files], _CLFS_IOSTATS_CLASS, clfs/CLFS_IOSTATS_CLASS, clfs/ClfsIoStatsDefault, clfs/ClfsIoStatsMax, clfs/PCLFS_IOSTATS_CLASS, clfs/PPCLFS_IOSTATS_CLASS, fs.clfs_iostats_class"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: CLFS_IOSTATS_CLASS, *PCLFS_IOSTATS_CLASS, PPCLFS_IOSTATS_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Clfs.h
api_name:
 - CLFS_IOSTATS_CLASS
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# _CLFS_IOSTATS_CLASS enumeration


## -description


Defines types of I/O statistics reported by CLFS and is used when a client calls <a href="https://msdn.microsoft.com/1d4a5486-8a9e-480a-952c-12fc7386af3e">GetLogIoStatistics</a>.  Currently, log flush rates are the only type of statistic reported, but this enumeration will reflect more types of statistics in the future.


## -enum-fields




### -field ClfsIoStatsDefault

The default I/O statistics exported.


### -field ClfsIoStatsMax

The log flush rate.


## -see-also




<a href="https://msdn.microsoft.com/1d4a5486-8a9e-480a-952c-12fc7386af3e">GetLogIoStatistics</a>
 

 

