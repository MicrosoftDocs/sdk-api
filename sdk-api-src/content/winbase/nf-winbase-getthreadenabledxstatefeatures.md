---
UID: NF:winbase.GetThreadEnabledXStateFeatures
tech.root: 
title: GetThreadEnabledXStateFeatures
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
 - GetThreadEnabledXStateFeatures
f1_keywords:
 - GetThreadEnabledXStateFeatures
 - winbase/GetThreadEnabledXStateFeatures
dev_langs:
 - c++
---

## -description

This function returns the set of XState features that are currently enabled for the current thread.

## -returns

The return value is a bitmask in which each bit represents an XState feature that is currently enabled for the current thread.

## -remarks

This function is related to <a href="/windows/desktop/api/winbase/nf-winbase-getenabledxstatefeatures">GetEnabledXStateFeatures</a>, which returns the set of XState features enabled in the system.
Prior to the introduction of optional XState features, the set of enabled XState features is the same for every thread in the system because all supported features are always enabled, thus the result returned from GetEnabledXStateFeatures and this function are identical.
With optional XState features, it is possible for optional XState features to be disabled by default for newly created threads and enabled on demand later. Optional XState features that are currently disabled for the current thread will not be returned by this function, but will still be returned by GetEnabledXStateFeatures.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getenabledxstatefeatures">GetEnabledXStateFeatures</a>

<a href="/windows/desktop/api/winbase/nf-winbase-enableprocessoptionalxstatefeatures">EnableProcessOptionalXStateFeatures</a>
