---
UID: NF:rtworkq.RtwqGetWorkQueueMMCSSPriority
title: RtwqGetWorkQueueMMCSSPriority function
author: windows-sdk-content
description: Gets the relative thread priority of a work queue.
old-location: base\rtwqgetworkqueuemmcsspriority.htm
tech.root: procthread
ms.assetid: c9f18299-bd0a-4c1c-acc0-2cc8bc84aa82
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: RtwqGetWorkQueueMMCSSPriority, RtwqGetWorkQueueMMCSSPriority function, base.rtwqgetworkqueuemmcsspriority, rtworkq/RtwqGetWorkQueueMMCSSPriority
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
 - RtwqGetWorkQueueMMCSSPriority
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RtwqGetWorkQueueMMCSSPriority
: 
---

# RtwqGetWorkQueueMMCSSPriority function


## -description


Gets the relative thread priority of a work queue.


## -parameters




### -param workQueueId [in]

The identifier of the work queue. For private work queues, the identifier is returned by the <a href="https://msdn.microsoft.com/B8FF907A-1448-43A4-B249-9D3D859D8F95">RtwqAllocateWorkQueue</a> function. 


### -param priority [out]

Receives the relative thread priority.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function returns the relative thread priority set by the <a href="https://msdn.microsoft.com/3012EFE9-437A-4B60-98DD-7602CD9A9E76">RtwqBeginRegisterWorkQueueWithMMCSS</a> function.



