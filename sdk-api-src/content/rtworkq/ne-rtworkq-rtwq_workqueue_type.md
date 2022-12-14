---
UID: NE:rtworkq.__unnamed_enum_0
title: RTWQ_WORKQUEUE_TYPE (rtworkq.h)
description: Specifies the type of work queue for the RtwqAllocateWorkQueue function to create.
helpviewer_keywords: ["RTWQ_MULTITHREADED_WORKQUEUE","RTWQ_STANDARD_WORKQUEUE","RTWQ_WINDOW_WORKQUEUE","RTWQ_WORKQUEUE_TYPE","RTWQ_WORKQUEUE_TYPE enumeration","base.rtwq_workqueue_type","rtworkq/RTWQ_MULTITHREADED_WORKQUEUE","rtworkq/RTWQ_STANDARD_WORKQUEUE","rtworkq/RTWQ_WINDOW_WORKQUEUE","rtworkq/RTWQ_WORKQUEUE_TYPE"]
old-location: base\rtwq_workqueue_type.htm
tech.root: backup
ms.assetid: 4aab85f3-855e-4fbf-9d25-209214bdd73b
ms.date: 12/05/2018
ms.keywords: RTWQ_MULTITHREADED_WORKQUEUE, RTWQ_STANDARD_WORKQUEUE, RTWQ_WINDOW_WORKQUEUE, RTWQ_WORKQUEUE_TYPE, RTWQ_WORKQUEUE_TYPE enumeration, base.rtwq_workqueue_type, rtworkq/RTWQ_MULTITHREADED_WORKQUEUE, rtworkq/RTWQ_STANDARD_WORKQUEUE, rtworkq/RTWQ_WINDOW_WORKQUEUE, rtworkq/RTWQ_WORKQUEUE_TYPE
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RTWQ_WORKQUEUE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RTWQ_WORKQUEUE_TYPE
 - rtworkq/RTWQ_WORKQUEUE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RTWorkQ.h
api_name:
 - RTWQ_WORKQUEUE_TYPE
---

# RTWQ_WORKQUEUE_TYPE enumeration


## -description

Specifies the type of work queue for the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqallocateworkqueue">RtwqAllocateWorkQueue</a> function to create.

## -enum-fields

### -field RTWQ_STANDARD_WORKQUEUE:0

Create a work queue without a message loop.

### -field RTWQ_WINDOW_WORKQUEUE:1

Create a work queue with a message loop.

### -field RTWQ_MULTITHREADED_WORKQUEUE:2

Create a multithreaded work queue. This type of work queue uses a thread pool to dispatch work items. The caller is responsible for serializing the work items.
