---
UID: NF:rtworkq.RtwqGetWorkQueueMMCSSClass
title: RtwqGetWorkQueueMMCSSClass function (rtworkq.h)
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) class currently associated with this work queue. (RtwqGetWorkQueueMMCSSClass)
helpviewer_keywords: ["RtwqGetWorkQueueMMCSSClass","RtwqGetWorkQueueMMCSSClass function","base.rtwqgetworkqueuemmcssclass","rtworkq/RtwqGetWorkQueueMMCSSClass"]
old-location: base\rtwqgetworkqueuemmcssclass.htm
tech.root: backup
ms.assetid: 1fea099d-33cd-4edd-aa6c-026a0e3478e3
ms.date: 12/05/2018
ms.keywords: RtwqGetWorkQueueMMCSSClass, RtwqGetWorkQueueMMCSSClass function, base.rtwqgetworkqueuemmcssclass, rtworkq/RtwqGetWorkQueueMMCSSClass
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtwqGetWorkQueueMMCSSClass
 - rtworkq/RtwqGetWorkQueueMMCSSClass
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqGetWorkQueueMMCSSClass
---

# RtwqGetWorkQueueMMCSSClass function


## -description

Retrieves the Multimedia Class Scheduler Service (MMCSS) class currently associated with this work queue.

## -parameters

### -param workQueueId [in]

Identifier for the work queue. The identifier is retrieved by the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqallocateworkqueue">RtwqAllocateWorkQueue</a> function.

### -param usageClass [out]

Pointer to a buffer that receives the name of the MMCSS class. This parameter can be <b>NULL</b>.

### -param usageClassLength [in, out]

On input, specifies the size of the <i>usageClass</i> buffer, in characters. On output, receives the required size of the buffer, in characters. The size includes the terminating null character.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
