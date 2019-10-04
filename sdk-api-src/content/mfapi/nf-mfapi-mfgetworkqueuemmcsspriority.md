---
UID: NF:mfapi.MFGetWorkQueueMMCSSPriority
title: MFGetWorkQueueMMCSSPriority function (mfapi.h)
author: windows-sdk-content
description: Gets the relative thread priority of a work queue.
old-location: mf\mfgetworkqueuemmcsspriority.htm
tech.root: medfound
ms.assetid: 8ADF4751-3BC5-4353-9927-C7E0079D0B83
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFGetWorkQueueMMCSSPriority, MFGetWorkQueueMMCSSPriority function [Media Foundation], mf.mfgetworkqueuemmcsspriority, mfapi/MFGetWorkQueueMMCSSPriority, mfplat/MFGetWorkQueueMMCSSPriority
ms.topic: function
f1_keywords: 
 - "mfapi/MFGetWorkQueueMMCSSPriority"
dev_langs:
 - c++
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
req.lib: 
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFGetWorkQueueMMCSSPriority
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFGetWorkQueueMMCSSPriority function


## -description


Gets the relative thread priority of a work queue.


## -parameters




### -param dwWorkQueueId [in]

The identifier of the work queue. For private work queues, the identifier is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> function. For platform work queues, see <a href="https://docs.microsoft.com/windows/desktop/medfound/work-queue-identifiers">Work Queue Identifiers</a>.


### -param lPriority [out]

Receives the relative thread priority.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function returns the relative thread priority set by the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex">MFBeginRegisterWorkQueueWithMMCSSEx</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-work-queue-and-threading-improvements">Work Queue and Threading Improvements</a>
 

 

