---
UID: NF:rtworkq.RtwqGetWorkQueueMMCSSClass
title: RtwqGetWorkQueueMMCSSClass function
author: windows-sdk-content
description: Retrieves the Multimedia Class Scheduler Service (MMCSS) class currently associated with this work queue.
old-location: base\rtwqgetworkqueuemmcssclass.htm
tech.root: ProcThread
ms.assetid: 1fea099d-33cd-4edd-aa6c-026a0e3478e3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: RtwqGetWorkQueueMMCSSClass, RtwqGetWorkQueueMMCSSClass function, base.rtwqgetworkqueuemmcssclass, rtworkq/RtwqGetWorkQueueMMCSSClass
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
 - RtwqGetWorkQueueMMCSSClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RtwqGetWorkQueueMMCSSClass
: 
---

# RtwqGetWorkQueueMMCSSClass function


## -description



Retrieves the Multimedia Class Scheduler Service (MMCSS) class currently associated with this work queue.




## -parameters




### -param workQueueId [in]

Identifier for the work queue. The identifier is retrieved by the <a href="https://msdn.microsoft.com/B8FF907A-1448-43A4-B249-9D3D859D8F95">RtwqAllocateWorkQueue</a> function.


### -param usageClass [out]

Pointer to a buffer that receives the name of the MMCSS class. This parameter can be <b>NULL</b>.


### -param usageClassLength [in, out]

On input, specifies the size of the <i>usageClass</i> buffer, in characters. On output, receives the required size of the buffer, in characters. The size includes the terminating null character.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



