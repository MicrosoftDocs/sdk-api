---
UID: NE:mfapi.MFASYNC_WORKQUEUE_TYPE
title: MFASYNC_WORKQUEUE_TYPE
author: windows-sdk-content
description: Specifies the type of work queue for the MFAllocateWorkQueueEx function to create.
old-location: mf\mfasync_workqueue_type.htm
tech.root: medfound
ms.assetid: a3627dbc-1794-4e2e-b7ed-869ed50ca893
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFASYNC_WORKQUEUE_TYPE, MFASYNC_WORKQUEUE_TYPE enumeration [Media Foundation], MF_MULTITHREADED_WORKQUEUE, MF_STANDARD_WORKQUEUE, MF_WINDOW_WORKQUEUE, mf.mfasync_workqueue_type, mfapi/MFASYNC_WORKQUEUE_TYPE, mfapi/MF_MULTITHREADED_WORKQUEUE, mfapi/MF_STANDARD_WORKQUEUE, mfapi/MF_WINDOW_WORKQUEUE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFASYNC_WORKQUEUE_TYPE
product: Windows
targetos: Windows
req.typenames: MFASYNC_WORKQUEUE_TYPE
req.redist: 
---

# MFASYNC_WORKQUEUE_TYPE enumeration


## -description


Specifies the type of work queue for the <a href="https://msdn.microsoft.com/422b8bc2-0616-4f7f-9908-775940f8c1ab">MFAllocateWorkQueueEx</a> function to create.


## -enum-fields




### -field MF_STANDARD_WORKQUEUE

Create a work queue without a message loop.


### -field MF_WINDOW_WORKQUEUE

Create a work queue with a message loop.


### -field MF_MULTITHREADED_WORKQUEUE

Create a multithreaded work queue. This type of work queue uses a thread pool to dispatch work items. The caller is responsible for serializing the work items.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/f886d096-b1f5-42e4-8888-501b58bffd50">Work Queues</a>
 

 

