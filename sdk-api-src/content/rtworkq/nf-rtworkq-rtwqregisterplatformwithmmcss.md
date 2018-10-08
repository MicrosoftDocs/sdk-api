---
UID: NF:rtworkq.RtwqRegisterPlatformWithMMCSS
title: RtwqRegisterPlatformWithMMCSS function
author: windows-sdk-content
description: Registers the standard platform work queues with the Multimedia Class Scheduler Service (MMCSS).
old-location: base\rtwqregisterplatformwithmmcss.htm
tech.root: procthread
ms.assetid: 17ba1e77-f1b0-4575-b96c-bf42813279ce
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: RtwqRegisterPlatformWithMMCSS, RtwqRegisterPlatformWithMMCSS function, base.rtwqregisterplatformwithmmcss, rtworkq/RtwqRegisterPlatformWithMMCSS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqRegisterPlatformWithMMCSS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



