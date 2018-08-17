---
UID: NE:rtworkq.RTWQ_WORKQUEUE_TYPE
title: RTWQ_WORKQUEUE_TYPE
author: windows-sdk-content
description: Specifies the type of work queue for the RtwqAllocateWorkQueue function to create.
old-location: base\rtwq_workqueue_type.htm
old-project: procthread
ms.assetid: 4aab85f3-855e-4fbf-9d25-209214bdd73b
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: RTWQ_MULTITHREADED_WORKQUEUE, RTWQ_STANDARD_WORKQUEUE, RTWQ_WINDOW_WORKQUEUE, RTWQ_WORKQUEUE_TYPE, RTWQ_WORKQUEUE_TYPE enumeration, base.rtwq_workqueue_type, rtworkq/RTWQ_MULTITHREADED_WORKQUEUE, rtworkq/RTWQ_STANDARD_WORKQUEUE, rtworkq/RTWQ_WINDOW_WORKQUEUE, rtworkq/RTWQ_WORKQUEUE_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: rtworkq.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RTWQ_WORKQUEUE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RTWorkQ.h
api_name:
 - RTWQ_WORKQUEUE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# RTWQ_WORKQUEUE_TYPE enumeration


## -description


Specifies the type of work queue for the <a href="https://msdn.microsoft.com/B8FF907A-1448-43A4-B249-9D3D859D8F95">RtwqAllocateWorkQueue</a> function to create.


## -enum-fields




### -field RTWQ_STANDARD_WORKQUEUE

Create a work queue without a message loop.


### -field RTWQ_WINDOW_WORKQUEUE

Create a work queue with a message loop.


### -field RTWQ_MULTITHREADED_WORKQUEUE

Create a multithreaded work queue. This type of work queue uses a thread pool to dispatch work items. The caller is responsible for serializing the work items.

