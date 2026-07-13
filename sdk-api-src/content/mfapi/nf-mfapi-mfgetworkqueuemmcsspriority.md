---
UID: NF:mfapi.MFGetWorkQueueMMCSSPriority
title: MFGetWorkQueueMMCSSPriority function (mfapi.h)
description: Gets the relative thread priority of a work queue. (MFGetWorkQueueMMCSSPriority)
helpviewer_keywords: ["MFGetWorkQueueMMCSSPriority","MFGetWorkQueueMMCSSPriority function [Media Foundation]","mf.mfgetworkqueuemmcsspriority","mfapi/MFGetWorkQueueMMCSSPriority","mfplat/MFGetWorkQueueMMCSSPriority"]
old-location: mf\mfgetworkqueuemmcsspriority.htm
tech.root: mf
ms.assetid: 8ADF4751-3BC5-4353-9927-C7E0079D0B83
ms.date: 12/05/2018
ms.keywords: MFGetWorkQueueMMCSSPriority, MFGetWorkQueueMMCSSPriority function [Media Foundation], mf.mfgetworkqueuemmcsspriority, mfapi/MFGetWorkQueueMMCSSPriority, mfplat/MFGetWorkQueueMMCSSPriority
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
 - MFGetWorkQueueMMCSSPriority
 - mfapi/MFGetWorkQueueMMCSSPriority
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
 - MFGetWorkQueueMMCSSPriority
---

# MFGetWorkQueueMMCSSPriority function


## -description

Gets the relative thread priority of a work queue.

## -parameters

### -param dwWorkQueueId [in]

The identifier of the work queue. For private work queues, the identifier is returned by the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> function. For platform work queues, see <a href="/windows/desktop/medfound/work-queue-identifiers">Work Queue Identifiers</a>.

### -param lPriority [out]

Receives the relative thread priority.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function returns the relative thread priority set by the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex">MFBeginRegisterWorkQueueWithMMCSSEx</a> function.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-foundation-work-queue-and-threading-improvements">Work Queue and Threading Improvements</a>
