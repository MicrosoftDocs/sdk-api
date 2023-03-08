---
UID: NF:ktmw32.PrepareComplete
title: PrepareComplete function (ktmw32.h)
description: Indicates that the resource manager (RM) has completed all processing necessary to guarantee that a commit or abort operation will succeed for the specified transaction.
helpviewer_keywords: ["PrepareComplete","PrepareComplete function [Files]","fs.preparecomplete","ktmw32/PrepareComplete"]
old-location: fs\preparecomplete.htm
tech.root: fs
ms.assetid: 47488c70-3409-4544-bcca-3415f91e7194
ms.date: 12/05/2018
ms.keywords: PrepareComplete, PrepareComplete function [Files], fs.preparecomplete, ktmw32/PrepareComplete
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
 - PrepareComplete
 - ktmw32/PrepareComplete
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
 - PrepareComplete
---

# PrepareComplete function


## -description

Indicates that the resource manager (RM) has completed all processing necessary to guarantee that a commit or abort operation will succeed for the specified transaction.

## -parameters

### -param EnlistmentHandle [in]

A handle to the enlistment.

### -param TmVirtualClock [in]

The latest virtual clock value received for this prepare complete notification. If you specify <b>NULL</b>, the virtual clock value is not changed. See <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>.

To change the virtual clock value, this value must be greater than the current value returned in the COMMIT notification.

## -returns

If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

 The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getcurrentclocktransactionmanager">GetCurrentClockTransactionManager</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanager">GetNotificationResourceManager</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanagerasync">GetNotificationResourceManagerAsync</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-prepreparecomplete">PrePrepareComplete</a>