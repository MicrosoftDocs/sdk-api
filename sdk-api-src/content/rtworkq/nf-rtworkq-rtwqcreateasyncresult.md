---
UID: NF:rtworkq.RtwqCreateAsyncResult
title: RtwqCreateAsyncResult function (rtworkq.h)
description: Creates an asynchronous result object. Use this function if you are implementing an asynchronous method. (RtwqCreateAsyncResult)
helpviewer_keywords: ["RtwqCreateAsyncResult","RtwqCreateAsyncResult function","base.rtwqcreateasyncresult","rtworkq/RtwqCreateAsyncResult"]
old-location: base\rtwqcreateasyncresult.htm
tech.root: backup
ms.assetid: ba8e888a-5bd6-4624-94a6-2f2ce0a080d1
ms.date: 12/05/2018
ms.keywords: RtwqCreateAsyncResult, RtwqCreateAsyncResult function, base.rtwqcreateasyncresult, rtworkq/RtwqCreateAsyncResult
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
 - RtwqCreateAsyncResult
 - rtworkq/RtwqCreateAsyncResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RTWorkQ.dll
api_name:
 - RtwqCreateAsyncResult
---

# RtwqCreateAsyncResult function


## -description

Creates an asynchronous result object. Use this function if you are implementing an asynchronous method.

## -parameters

### -param appObject [in]

Pointer to the object stored in the asynchronous result. This pointer is returned by the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-irtwqasyncresult-getobject">IRtwqAsyncResult::GetObject</a> method. This parameter can be <b>NULL</b>.

### -param callback [in]

Pointer to the <a href="/windows/desktop/api/rtworkq/nn-rtworkq-irtwqasynccallback">IRtwqAsyncCallback</a> interface. This interface is implemented by the caller of the asynchronous method.

### -param appState [in]

Pointer to the <b>IUnknown</b> interface of a state object. This value is provided by the caller of the asynchronous method. This parameter can be <b>NULL</b>.

### -param asyncResult [out]

Receives a pointer to the <a href="/windows/desktop/api/rtworkq/nn-rtworkq-irtwqasyncresult">IRtwqAsyncResult</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To invoke the callback specified in <i>pCallback</i>, call the <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqinvokecallback">RtwqInvokeCallback</a> function.
