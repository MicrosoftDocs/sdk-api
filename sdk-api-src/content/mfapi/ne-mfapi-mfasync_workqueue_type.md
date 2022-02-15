---
UID: NE:mfapi.__unnamed_enum_0
title: MFASYNC_WORKQUEUE_TYPE (mfapi.h)
description: Specifies the type of work queue for the MFAllocateWorkQueueEx function to create.
helpviewer_keywords: ["MFASYNC_WORKQUEUE_TYPE","MFASYNC_WORKQUEUE_TYPE enumeration [Media Foundation]","MF_MULTITHREADED_WORKQUEUE","MF_STANDARD_WORKQUEUE","MF_WINDOW_WORKQUEUE","mf.mfasync_workqueue_type","mfapi/MFASYNC_WORKQUEUE_TYPE","mfapi/MF_MULTITHREADED_WORKQUEUE","mfapi/MF_STANDARD_WORKQUEUE","mfapi/MF_WINDOW_WORKQUEUE"]
old-location: mf\mfasync_workqueue_type.htm
tech.root: mf
ms.assetid: a3627dbc-1794-4e2e-b7ed-869ed50ca893
ms.date: 12/05/2018
ms.keywords: MFASYNC_WORKQUEUE_TYPE, MFASYNC_WORKQUEUE_TYPE enumeration [Media Foundation], MF_MULTITHREADED_WORKQUEUE, MF_STANDARD_WORKQUEUE, MF_WINDOW_WORKQUEUE, mf.mfasync_workqueue_type, mfapi/MFASYNC_WORKQUEUE_TYPE, mfapi/MF_MULTITHREADED_WORKQUEUE, mfapi/MF_STANDARD_WORKQUEUE, mfapi/MF_WINDOW_WORKQUEUE
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
targetos: Windows
req.typenames: MFASYNC_WORKQUEUE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFASYNC_WORKQUEUE_TYPE
 - mfapi/MFASYNC_WORKQUEUE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFASYNC_WORKQUEUE_TYPE
---

# MFASYNC_WORKQUEUE_TYPE enumeration


## -description

Specifies the type of work queue for the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueueex">MFAllocateWorkQueueEx</a> function to create.

## -enum-fields

### -field MF_STANDARD_WORKQUEUE:0

Create a work queue without a message loop.

### -field MF_WINDOW_WORKQUEUE:1

Create a work queue with a message loop.

### -field MF_MULTITHREADED_WORKQUEUE:2

Create a multithreaded work queue. This type of work queue uses a thread pool to dispatch work items. The caller is responsible for serializing the work items.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="/windows/desktop/medfound/work-queues">Work Queues</a>
