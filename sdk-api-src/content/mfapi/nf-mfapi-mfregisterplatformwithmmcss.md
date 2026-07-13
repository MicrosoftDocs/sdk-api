---
UID: NF:mfapi.MFRegisterPlatformWithMMCSS
title: MFRegisterPlatformWithMMCSS function (mfapi.h)
description: Registers the standard Microsoft Media Foundation platform work queues with the Multimedia Class Scheduler Service (MMCSS).
helpviewer_keywords: ["MFRegisterPlatformWithMMCSS","MFRegisterPlatformWithMMCSS function [Media Foundation]","mf.mfregisterplatformwithmmcss","mfapi/MFRegisterPlatformWithMMCSS","mfplat/MFRegisterPlatformWithMMCSS"]
old-location: mf\mfregisterplatformwithmmcss.htm
tech.root: mf
ms.assetid: 8F99849B-5363-4EEF-BCB8-C69A5309AF34
ms.date: 12/05/2018
ms.keywords: MFRegisterPlatformWithMMCSS, MFRegisterPlatformWithMMCSS function [Media Foundation], mf.mfregisterplatformwithmmcss, mfapi/MFRegisterPlatformWithMMCSS, mfplat/MFRegisterPlatformWithMMCSS
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFRegisterPlatformWithMMCSS
 - mfapi/MFRegisterPlatformWithMMCSS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFRegisterPlatformWithMMCSS
---

# MFRegisterPlatformWithMMCSS function


## -description

Registers the standard Microsoft Media Foundation platform work queues with the Multimedia Class Scheduler Service (MMCSS).

## -parameters

### -param wszClass [in]

The name of the MMCSS task.

### -param pdwTaskId [in, out]

The MMCSS task identifier. On input, specify an existing  MCCSS task group ID, or use the value zero to create a new task group. On output, receives the actual task group ID.

### -param lPriority [in]

The base priority of the work-queue threads.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To unregister the platform work queues from the MMCSS class, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfunregisterplatformfrommmcss">MFUnregisterPlatformFromMMCSS</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-foundation-work-queue-and-threading-improvements">Work Queue and Threading Improvements</a>