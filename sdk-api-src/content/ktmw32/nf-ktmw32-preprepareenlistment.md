---
UID: NF:ktmw32.PrePrepareEnlistment
title: PrePrepareEnlistment function (ktmw32.h)
author: windows-sdk-content
description: Pre-prepares the transaction associated with this enlistment handle. This function is used by communication resource managers (sometimes called superior transaction managers).
old-location: fs\preprepareenlistment.htm
tech.root: ktm
ms.assetid: 7a336267-4bee-4aac-abff-ec112650789a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PrePrepareEnlistment, PrePrepareEnlistment function [Files], fs.preprepareenlistment, ktmw32/PrePrepareEnlistment
ms.topic: function
req.header: ktmw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: KtmW32.lib
req.dll: KtmW32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KtmW32.dll
api_name:
 - PrePrepareEnlistment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PrePrepareEnlistment function


## -description


Pre-prepares the transaction associated with this enlistment handle. This function is used by 
    communication resource managers (sometimes called superior transaction managers).


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment for which the prepare operation has completed.


### -param TmVirtualClock [in]

A pointer to the latest virtual clock value received for this transaction.


## -returns



If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero (0). To get extended error information, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/21d7c0fa-3a49-43b3-9325-d3dfdabbcb98">GetCurrentClockTransactionManager</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/5f1b1eb2-e2f5-4daf-b549-7f0c195414f0">PrepareEnlistment</a>



<a href="https://msdn.microsoft.com/a6411fad-8ad0-4a31-9e09-0c18dd384634">ReadOnlyEnlistment</a>



<a href="https://msdn.microsoft.com/8cc77686-e130-4b82-b2f5-70121b40e052">SinglePhaseReject</a>
 

 

