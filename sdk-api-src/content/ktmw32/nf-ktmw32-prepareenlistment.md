---
UID: NF:ktmw32.PrepareEnlistment
title: PrepareEnlistment function (ktmw32.h)
description: Prepares the transaction associated with this enlistment handle. This function is used by communication resource managers (sometimes called superior transaction managers).
old-location: fs\prepareenlistment.htm
tech.root: ktm
ms.assetid: 5f1b1eb2-e2f5-4daf-b549-7f0c195414f0
ms.date: 12/05/2018
ms.keywords: PrepareEnlistment, PrepareEnlistment function [Files], fs.prepareenlistment, ktmw32/PrepareEnlistment
ms.topic: function
f1_keywords:
- ktmw32/PrepareEnlistment
dev_langs:
- c++
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
- PrepareEnlistment
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PrepareEnlistment function


## -description


Prepares the transaction associated with this enlistment handle. This function is used by 
    communication resource managers (sometimes called superior transaction managers).


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment for which the prepare operation has completed.


### -param TmVirtualClock [in]

A pointer to the latest virtual clock value received for this transaction.


## -returns



If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero (0). To get extended error information, call the 
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the possible error codes:




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-getcurrentclocktransactionmanager">GetCurrentClockTransactionManager</a>



<a href="https://docs.microsoft.com/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-preprepareenlistment">PrePrepareEnlistment</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-readonlyenlistment">ReadOnlyEnlistment</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-singlephasereject">SinglePhaseReject</a>
 

 

