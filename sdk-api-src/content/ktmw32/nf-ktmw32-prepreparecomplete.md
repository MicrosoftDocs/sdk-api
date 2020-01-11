---
UID: NF:ktmw32.PrePrepareComplete
title: PrePrepareComplete function (ktmw32.h)
description: Signals that this resource manager has completed its preprepare work, so that other resource managers can now begin their prepare operations.
old-location: fs\prepreparecomplete.htm
tech.root: ktm
ms.assetid: b4a70a51-2c49-4626-9fca-9ca6e0d21a53
ms.date: 12/05/2018
ms.keywords: PrePrepareComplete, PrePrepareComplete function [Files], fs.prepreparecomplete, ktmw32/PrePrepareComplete
f1_keywords:
- ktmw32/PrePrepareComplete
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ktmw32.dll
api_name:
- PrePrepareComplete
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PrePrepareComplete function


## -description


Signals that this resource manager has completed its preprepare work, so that other   resource managers can now begin their prepare operations.


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment.


### -param TmVirtualClock [in]

The latest virtual clock value received for this preprepare operation. If you specify <b>NULL</b>, the virtual clock value is not changed. See <a href="https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-large_integer~r1">LARGE_INTEGER</a>.

To change the virtual clock value, this value must be greater than the current value returned in the COMMIT notification.


## -returns



If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

 The following list identifies the possible error codes:




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-getcurrentclocktransactionmanager">GetCurrentClockTransactionManager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanager">GetNotificationResourceManager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanagerasync">GetNotificationResourceManagerAsync</a>



<a href="https://docs.microsoft.com/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-preparecomplete">PrepareComplete</a>
 

 

