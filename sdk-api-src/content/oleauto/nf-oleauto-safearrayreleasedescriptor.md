---
UID: NF:oleauto.SafeArrayReleaseDescriptor
title: SafeArrayReleaseDescriptor function (oleauto.h)
description: Decreases the pinning reference count for the descriptor of the specified safe array by one. When that count reaches 0, the memory for that descriptor is no longer prevented from being freed.
helpviewer_keywords: ["SafeArrayReleaseDescriptor","SafeArrayReleaseDescriptor function [Automation]","automat.safearrayreleasedescriptor","oleauto/SafeArrayReleaseDescriptor"]
old-location: automat\safearrayreleasedescriptor.htm
tech.root: automat
ms.assetid: D6678B17-B537-46CF-AC64-4D0C0DC4CDF3
ms.date: 12/05/2018
ms.keywords: SafeArrayReleaseDescriptor, SafeArrayReleaseDescriptor function [Automation], automat.safearrayreleasedescriptor, oleauto/SafeArrayReleaseDescriptor
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mincore.lib
req.dll: Oleaut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SafeArrayReleaseDescriptor
 - oleauto/SafeArrayReleaseDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleaut32.dll
api_name:
 - SafeArrayReleaseDescriptor
---

# SafeArrayReleaseDescriptor function


## -description

<div class="alert"><b>Note</b>  You should only call <b>SafeArrayReleaseDescriptor</b> if you are implementing a scripting engine that needs to guard against running potentially malicious scripts.</div><div> </div>Decreases the pinning reference count for the descriptor of the specified safe array by one. When that count reaches 0, the memory for that descriptor is no longer prevented from being freed.

## -parameters

### -param psa [in]

The safe array for which the pinning reference count of the descriptor should decrease.

## -remarks

A call to the <b>SafeArrayReleaseDescriptor</b> function should match every previous call to the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayaddref">SafeArrayAddRef</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayaddref">SafeArrayAddRef</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayreleasedata">SafeArrayReleaseData</a>