---
UID: NF:winbase.GetCurrentUmsThread
title: GetCurrentUmsThread function (winbase.h)
description: Returns the user-mode scheduling (UMS) thread context of the calling UMS thread.
old-location: base\getcurrentumsthread.htm
tech.root: ProcThread
ms.assetid: f2e20816-919a-443d-96d3-94e98afc28f2
ms.date: 12/05/2018
ms.keywords: GetCurrentUmsThread, GetCurrentUmsThread function, base.getcurrentumsthread, winbase/GetCurrentUmsThread
f1_keywords:
- winbase/GetCurrentUmsThread
dev_langs:
- c++
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 (64-bit only) [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-ums-l1-1-0.dll
api_name:
- GetCurrentUmsThread
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCurrentUmsThread function


## -description


Returns the user-mode scheduling (UMS) thread context of the calling UMS thread.


## -parameters






## -returns



The function returns a pointer to the UMS thread context of the calling thread.

If calling thread is not a UMS thread, the function returns NULL. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



The <b>GetCurrentUmsThread</b> function can be called for a UMS scheduler thread or UMS worker thread.



