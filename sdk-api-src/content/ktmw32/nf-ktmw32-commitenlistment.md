---
UID: NF:ktmw32.CommitEnlistment
title: CommitEnlistment function (ktmw32.h)
description: Commits the transaction associated with this enlistment handle. This function is used by communication resource managers (sometimes called superior transaction managers).
helpviewer_keywords: ["CommitEnlistment","CommitEnlistment function [Files]","fs.commitenlistment","ktmw32/CommitEnlistment"]
old-location: fs\commitenlistment.htm
tech.root: fs
ms.assetid: d1e1043d-2db3-4f05-affc-2d32744baf10
ms.date: 12/05/2018
ms.keywords: CommitEnlistment, CommitEnlistment function [Files], fs.commitenlistment, ktmw32/CommitEnlistment
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
 - CommitEnlistment
 - ktmw32/CommitEnlistment
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
 - CommitEnlistment
---

# CommitEnlistment function


## -description

Commits the transaction associated with this enlistment handle. This function is used by communication 
    resource managers (sometimes called superior transaction managers).

## -parameters

### -param EnlistmentHandle [in]

A handle to the enlistment to commit.

### -param TmVirtualClock [in]

A pointer to the latest virtual clock value received for this enlistment. If you specify 
      <b>NULL</b>, the virtual clock value is not changed.

To change the virtual clock value, this value must be greater than the current value returned by a 
      subordinate TM.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.


The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-commitcomplete">CommitComplete</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createenlistment">CreateEnlistment</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getcurrentclocktransactionmanager">GetCurrentClockTransactionManager</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>