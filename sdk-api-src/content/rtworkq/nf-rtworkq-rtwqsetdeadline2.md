---
UID: NF:rtworkq.RtwqSetDeadline2
title: RtwqSetDeadline2 function
author: windows-sdk-content
description: Sets a deadline by which the work in a work queue must be completed.
old-location: base\rtwqsetdeadline2.htm
old-project: procthread
ms.assetid: A259C9D2-9700-4FE8-81D6-7AD14476AA9C
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: RtwqSetDeadline2, RtwqSetDeadline2 function, base.rtwqsetdeadline2, rtworkq/RtwqSetDeadline2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rtworkq.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: RTWQ_WORKQUEUE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqSetDeadline2
product: Windows
targetos: Windows
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
req.product: ADAM
---

# RtwqSetDeadline2 function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Sets a deadline by which the work in a work queue must be completed.


## -parameters




### -param workQueueId [in]

The identifier for the work queue. The identifier is returned by the <a href="https://msdn.microsoft.com/B8FF907A-1448-43A4-B249-9D3D859D8F95">RtwqAllocateWorkQueue</a> function. 


### -param deadlineInHNS [in]

 The deadline for the work in the queue to be completed, in milliseconds.


### -param preDeadlineInHNS [in]

 The pre-deadline for the work in the queue to be completed, in milliseconds.


### -param pRequest [in, out]

Receives a handle to the request that can be used to cancel the request by calling <a href="https://msdn.microsoft.com/4128B655-AFF9-4AEF-8EDB-A6DC8DA05FE9">RtwqCancelDeadline</a>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Update a deadline by creating a new deadline and releasing the old one.

Cancel a deadline by calling <a href="https://msdn.microsoft.com/4128B655-AFF9-4AEF-8EDB-A6DC8DA05FE9">RtwqCancelDeadline</a>.




## -see-also




<a href="https://msdn.microsoft.com/4128B655-AFF9-4AEF-8EDB-A6DC8DA05FE9">RtwqCancelDeadline</a>
 

 

