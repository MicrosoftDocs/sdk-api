---
UID: NS:projectedfslib.PRJ_STARTVIRTUALIZING_OPTIONS
title: PRJ_STARTVIRTUALIZING_OPTIONS (projectedfslib.h)
description: Options to provide when starting a virtualization instance.
helpviewer_keywords: ["PRJ_STARTVIRTUALIZING_OPTIONS","PRJ_STARTVIRTUALIZING_OPTIONS structure","ProjFS.prj_startvirtualizing_options","projectedfslib/PRJ_STARTVIRTUALIZING_OPTIONS"]
old-location: projfs\prj_startvirtualizing_options.htm
tech.root: ProjFS
ms.assetid: 5FF20B04-29A6-4310-ACD6-35E189B87C9E
ms.date: 12/05/2018
ms.keywords: PRJ_STARTVIRTUALIZING_OPTIONS, PRJ_STARTVIRTUALIZING_OPTIONS structure, ProjFS.prj_startvirtualizing_options, projectedfslib/PRJ_STARTVIRTUALIZING_OPTIONS
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
req.typenames: PRJ_STARTVIRTUALIZING_OPTIONS
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_STARTVIRTUALIZING_OPTIONS
 - projectedfslib/PRJ_STARTVIRTUALIZING_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - projectedfslib.h
api_name:
 - PRJ_STARTVIRTUALIZING_OPTIONS
---

# PRJ_STARTVIRTUALIZING_OPTIONS structure


## -description

Options to provide when starting a virtualization instance.

## -struct-fields

### -field Flags

A flag for starting virtualization.

### -field PoolThreadCount

The number of threads the provider wants to create to service callbacks.

### -field ConcurrentThreadCount

The maximum number of threads the provider wants to run concurrently to process callbacks.

### -field NotificationMappings

An array of zero or more notification mappings. See the Remarks section of PRJ_NOTIFICATION MAPPING for more details.

### -field NotificationMappingsCount

The number of notification mappings provided in NotificationMappings.

