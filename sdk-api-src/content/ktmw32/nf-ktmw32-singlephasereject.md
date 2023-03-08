---
UID: NF:ktmw32.SinglePhaseReject
title: SinglePhaseReject function (ktmw32.h)
description: Indicates that the resource manager (RM) is refusing a single-phase request. When a transaction manager (TM) receives this call, it initiates a two-phase commit and sends a prepare request to all enlisted RMs.
helpviewer_keywords: ["SinglePhaseReject","SinglePhaseReject function [Files]","fs.singlephasereject","ktmw32/SinglePhaseReject"]
old-location: fs\singlephasereject.htm
tech.root: fs
ms.assetid: 8cc77686-e130-4b82-b2f5-70121b40e052
ms.date: 12/05/2018
ms.keywords: SinglePhaseReject, SinglePhaseReject function [Files], fs.singlephasereject, ktmw32/SinglePhaseReject
req.header: ktmw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SinglePhaseReject
 - ktmw32/SinglePhaseReject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - SinglePhaseReject
---

# SinglePhaseReject function


## -description

Indicates that the resource manager (RM) is refusing a single-phase request. When a transaction manager (TM) receives this call, it initiates a two-phase commit and sends a prepare request to all enlisted RMs.

## -parameters

### -param EnlistmentHandle [in]

A handle to the enlistment.

### -param TmVirtualClock [in]

The latest virtual clock value received from the single-phase request notification. If you specify <b>NULL</b>, the virtual clock value is not changed. See <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>.

To change the virtual clock value, this value must be greater than the current value returned in the COMMIT notification.

## -returns

If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

 The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getcurrentclocktransactionmanager">GetCurrentClockTransactionManager</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>