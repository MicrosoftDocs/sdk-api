---
UID: NF:mfidl.IMFWorkQueueServicesEx.GetPlatformWorkQueueMMCSSPriority
title: IMFWorkQueueServicesEx::GetPlatformWorkQueueMMCSSPriority (mfidl.h)
description: Gets the priority of the Multimedia Class Scheduler Service (MMCSS) priority associated with the specified platform work queue.
helpviewer_keywords: ["GetPlatformWorkQueueMMCSSPriority","GetPlatformWorkQueueMMCSSPriority method [Media Foundation]","GetPlatformWorkQueueMMCSSPriority method [Media Foundation]","IMFWorkQueueServicesEx interface","IMFWorkQueueServicesEx interface [Media Foundation]","GetPlatformWorkQueueMMCSSPriority method","IMFWorkQueueServicesEx.GetPlatformWorkQueueMMCSSPriority","IMFWorkQueueServicesEx::GetPlatformWorkQueueMMCSSPriority","mf.imfworkqueueservicesex_getplatformworkqueuemmcsspriority","mfidl/IMFWorkQueueServicesEx::GetPlatformWorkQueueMMCSSPriority"]
old-location: mf\imfworkqueueservicesex_getplatformworkqueuemmcsspriority.htm
tech.root: mf
ms.assetid: e9271439-8785-4743-9e6f-81342af117f8
ms.date: 12/05/2018
ms.keywords: GetPlatformWorkQueueMMCSSPriority, GetPlatformWorkQueueMMCSSPriority method [Media Foundation], GetPlatformWorkQueueMMCSSPriority method [Media Foundation],IMFWorkQueueServicesEx interface, IMFWorkQueueServicesEx interface [Media Foundation],GetPlatformWorkQueueMMCSSPriority method, IMFWorkQueueServicesEx.GetPlatformWorkQueueMMCSSPriority, IMFWorkQueueServicesEx::GetPlatformWorkQueueMMCSSPriority, mf.imfworkqueueservicesex_getplatformworkqueuemmcsspriority, mfidl/IMFWorkQueueServicesEx::GetPlatformWorkQueueMMCSSPriority
req.header: mfidl.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFWorkQueueServicesEx::GetPlatformWorkQueueMMCSSPriority
 - mfidl/IMFWorkQueueServicesEx::GetPlatformWorkQueueMMCSSPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFWorkQueueServicesEx.GetPlatformWorkQueueMMCSSPriority
---

# IMFWorkQueueServicesEx::GetPlatformWorkQueueMMCSSPriority


## -description

Gets the priority of the Multimedia Class Scheduler Service (MMCSS)  priority associated with
    the specified platform work queue.

## -parameters

### -param dwPlatformWorkQueueId [in]

Topology work queue id for which the info will be returned.

### -param plPriority [out]

## -returns

Pointer to a buffer allocated by the caller
    that the work queue's MMCSS task id will be copied to.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex">IMFWorkQueueServicesEx</a>