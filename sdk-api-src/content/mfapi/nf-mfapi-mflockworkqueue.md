---
UID: NF:mfapi.MFLockWorkQueue
title: MFLockWorkQueue function (mfapi.h)
description: Locks a work queue.
old-location: mf\mflockworkqueue.htm
tech.root: medfound
ms.assetid: 307a1ec5-e54a-47f6-8ace-3b935081faf8
ms.date: 12/05/2018
ms.keywords: 307a1ec5-e54a-47f6-8ace-3b935081faf8, MFLockWorkQueue, MFLockWorkQueue function [Media Foundation], mf.mflockworkqueue, mfapi/MFLockWorkQueue
f1_keywords:
- mfapi/MFLockWorkQueue
dev_langs:
- c++
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- mfplat.dll
api_name:
- MFLockWorkQueue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFLockWorkQueue function


## -description


Locks a work queue.


## -parameters




### -param dwWorkQueue [in]

The identifier for the work queue. The identifier is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> function.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function prevents the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfshutdown">MFShutdown</a> function from shutting down the work queue. Use this function to ensure that asynchronous operations on the work queue complete gracefully before the platform shuts down. The <b>MFShutdown</b> function blocks until the work queue is unlocked, or until a fixed wait period has elapsed. (The wait period is a few seconds.)

Call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue">MFUnlockWorkQueue</a> to unlock the work queue. Each call to <b>MFLockWorkQueue</b> must be matched by a corresponding call to <b>MFUnlockWorkQueue</b>.


<div class="alert"><b>Note</b>  The <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue">MFAllocateWorkQueue</a> function implicitly locks the work queue that it creates.</div>
<div> </div>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/work-queues">Work Queues</a>
 

 

