---
UID: NF:mfidl.IMFWorkQueueServicesEx.GetTopologyWorkQueueMMCSSPriority
title: IMFWorkQueueServicesEx::GetTopologyWorkQueueMMCSSPriority (mfidl.h)
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) string associated with the given topology work queue.
helpviewer_keywords: ["GetTopologyWorkQueueMMCSSPriority","GetTopologyWorkQueueMMCSSPriority method [Media Foundation]","GetTopologyWorkQueueMMCSSPriority method [Media Foundation]","IMFWorkQueueServicesEx interface","IMFWorkQueueServicesEx interface [Media Foundation]","GetTopologyWorkQueueMMCSSPriority method","IMFWorkQueueServicesEx.GetTopologyWorkQueueMMCSSPriority","IMFWorkQueueServicesEx::GetTopologyWorkQueueMMCSSPriority","mf.imfworkqueueservicesex_gettopologyworkqueuemmcsspriority","mfidl/IMFWorkQueueServicesEx::GetTopologyWorkQueueMMCSSPriority"]
old-location: mf\imfworkqueueservicesex_gettopologyworkqueuemmcsspriority.htm
tech.root: mf
ms.assetid: d5550e53-cbe9-4956-a079-d2a825fd17ef
ms.date: 12/05/2018
ms.keywords: GetTopologyWorkQueueMMCSSPriority, GetTopologyWorkQueueMMCSSPriority method [Media Foundation], GetTopologyWorkQueueMMCSSPriority method [Media Foundation],IMFWorkQueueServicesEx interface, IMFWorkQueueServicesEx interface [Media Foundation],GetTopologyWorkQueueMMCSSPriority method, IMFWorkQueueServicesEx.GetTopologyWorkQueueMMCSSPriority, IMFWorkQueueServicesEx::GetTopologyWorkQueueMMCSSPriority, mf.imfworkqueueservicesex_gettopologyworkqueuemmcsspriority, mfidl/IMFWorkQueueServicesEx::GetTopologyWorkQueueMMCSSPriority
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
 - IMFWorkQueueServicesEx::GetTopologyWorkQueueMMCSSPriority
 - mfidl/IMFWorkQueueServicesEx::GetTopologyWorkQueueMMCSSPriority
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
 - IMFWorkQueueServicesEx.GetTopologyWorkQueueMMCSSPriority
---

# IMFWorkQueueServicesEx::GetTopologyWorkQueueMMCSSPriority


## -description

Retrieves the Multimedia Class Scheduler Service (MMCSS)  string associated with the given topology work queue.

## -parameters

### -param dwTopologyWorkQueueId [in]

The id of the topology work queue.

### -param plPriority [out]

Pointer to the buffer the work queue's MMCSS task id will be copied to.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex">IMFWorkQueueServicesEx</a>