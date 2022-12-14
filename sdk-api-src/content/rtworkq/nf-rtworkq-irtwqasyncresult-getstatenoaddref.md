---
UID: NF:rtworkq.IRtwqAsyncResult.GetStateNoAddRef
title: IRtwqAsyncResult::GetStateNoAddRef (rtworkq.h)
description: Returns the state object specified by the caller in the asynchronous Begin method, without incrementing the object's reference count. (IRtwqAsyncResult.GetStateNoAddRef)
helpviewer_keywords: ["GetStateNoAddRef","GetStateNoAddRef method","GetStateNoAddRef method","IRtwqAsyncResult interface","IRtwqAsyncResult interface","GetStateNoAddRef method","IRtwqAsyncResult.GetStateNoAddRef","IRtwqAsyncResult::GetStateNoAddRef","base.irtwqasyncresult_getstatenoaddref","rtworkq/IRtwqAsyncResult::GetStateNoAddRef"]
old-location: base\irtwqasyncresult_getstatenoaddref.htm
tech.root: backup
ms.assetid: DF41E4E7-015C-469A-A94F-16F06445B804
ms.date: 12/05/2018
ms.keywords: GetStateNoAddRef, GetStateNoAddRef method, GetStateNoAddRef method,IRtwqAsyncResult interface, IRtwqAsyncResult interface,GetStateNoAddRef method, IRtwqAsyncResult.GetStateNoAddRef, IRtwqAsyncResult::GetStateNoAddRef, base.irtwqasyncresult_getstatenoaddref, rtworkq/IRtwqAsyncResult::GetStateNoAddRef
req.header: rtworkq.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtworkq.lib
req.dll: RTWorkQ.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRtwqAsyncResult::GetStateNoAddRef
 - rtworkq/IRtwqAsyncResult::GetStateNoAddRef
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTWorkQ.dll
api_name:
 - IRtwqAsyncResult.GetStateNoAddRef
---

# IRtwqAsyncResult::GetStateNoAddRef


## -description

Returns the state object specified by the caller in the asynchronous <b>Begin</b> method, without incrementing the object's reference count.



## -returns

Returns a pointer to the state object's <b>IUnknown</b> interface, or <b>NULL</b> if no object was set. This pointer does not have an outstanding reference count. If you store this pointer, you must call <b>AddRef</b> on the pointer.

## -see-also

<a href="/windows/desktop/api/rtworkq/nn-rtworkq-irtwqasyncresult">IRtwqAsyncResult</a>
