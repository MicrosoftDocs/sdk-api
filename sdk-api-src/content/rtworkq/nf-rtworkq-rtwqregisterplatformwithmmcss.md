---
UID: NF:rtworkq.RtwqRegisterPlatformWithMMCSS
title: RtwqRegisterPlatformWithMMCSS function (rtworkq.h)
description: Registers the standard platform work queues with the Multimedia Class Scheduler Service (MMCSS).
helpviewer_keywords: ["RtwqRegisterPlatformWithMMCSS","RtwqRegisterPlatformWithMMCSS function","base.rtwqregisterplatformwithmmcss","rtworkq/RtwqRegisterPlatformWithMMCSS"]
old-location: base\rtwqregisterplatformwithmmcss.htm
tech.root: backup
ms.assetid: 17ba1e77-f1b0-4575-b96c-bf42813279ce
ms.date: 12/05/2018
ms.keywords: RtwqRegisterPlatformWithMMCSS, RtwqRegisterPlatformWithMMCSS function, base.rtwqregisterplatformwithmmcss, rtworkq/RtwqRegisterPlatformWithMMCSS
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtwqRegisterPlatformWithMMCSS
 - rtworkq/RtwqRegisterPlatformWithMMCSS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqRegisterPlatformWithMMCSS
---

# RtwqRegisterPlatformWithMMCSS function


## -description

Registers the standard platform work queues with the Multimedia Class Scheduler Service (MMCSS).

## -parameters

### -param usageClass [in]

The name of the MMCSS task.

### -param taskId [in, out]

The MMCSS task identifier. On input, specify an existing MCCSS task group ID, or use the value zero to create a new task group. On output, receives the actual task group ID.

### -param lPriority [in]

The base priority of the work-queue threads.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

