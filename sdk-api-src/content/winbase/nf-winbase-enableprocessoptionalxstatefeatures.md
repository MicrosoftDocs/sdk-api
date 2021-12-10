---
UID: NF:winbase.EnableProcessOptionalXStateFeatures
tech.root: 
title: EnableProcessOptionalXStateFeatures
ms.date: 
targetos: Windows
description: 
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: winbase.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11
req.target-min-winversvr: Windows Server 2022
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - 
api_location:
 - winbase.h
api_name:
 - EnableProcessOptionalXStateFeatures
f1_keywords:
 - EnableProcessOptionalXStateFeatures
 - winbase/EnableProcessOptionalXStateFeatures
dev_langs:
 - c++
---

## -description

This function enables a set of optional XState features for the current process.

## -parameters

### -param Features

A bitmask in which each bit represents an optional XState feature to enable for the current process.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

In general, optional XState features are disabled by default for newly created threads and enabled on demand later.
When this function returns, the specified optional XState features will be enabled for all existing threads in the current process, and all future threads created in the process will have the specified optional XState features enabled at thread creation time.

Only XState feature bits supported by the system are allowed to be supplied to this function, otherwise an error is returned. The XState feature bits supported by the system can be obtained via the <a href="/windows/desktop/api/winbase/nf-winbase-getenabledxstatefeatures">GetEnabledXStateFeatures</a> routine.
If non-optional XState feature bits supported by the system are supplied (for example AVX, AVX2, etc. are non-optional XState features), those are ignored and will not cause this function to return an error. Note that all non-optional XState features supported by the system are always enabled for every thread by default.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getenabledxstatefeatures">GetEnabledXStateFeatures</a>

<a href="/windows/desktop/api/winbase/nf-winbase-getthreadenabledxstatefeatures">GetThreadEnabledXStateFeatures</a>
