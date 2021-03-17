---
UID: NF:ktmw32.PrePrepareEnlistment
title: PrePrepareEnlistment function (ktmw32.h)
description: Pre-prepares the transaction associated with this enlistment handle. This function is used by communication resource managers (sometimes called superior transaction managers).
helpviewer_keywords: ["PrePrepareEnlistment","PrePrepareEnlistment function [Files]","fs.preprepareenlistment","ktmw32/PrePrepareEnlistment"]
old-location: fs\preprepareenlistment.htm
tech.root: fs
ms.assetid: 7a336267-4bee-4aac-abff-ec112650789a
ms.date: 12/05/2018
ms.keywords: PrePrepareEnlistment, PrePrepareEnlistment function [Files], fs.preprepareenlistment, ktmw32/PrePrepareEnlistment
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PrePrepareEnlistment
 - ktmw32/PrePrepareEnlistment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KtmW32.dll
api_name:
 - PrePrepareEnlistment
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
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getcurrentclocktransactionmanager">GetCurrentClockTransactionManager</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-prepareenlistment">PrepareEnlistment</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-readonlyenlistment">ReadOnlyEnlistment</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-singlephasereject">SinglePhaseReject</a>