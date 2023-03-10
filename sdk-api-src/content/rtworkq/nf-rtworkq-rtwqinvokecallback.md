---
UID: NF:rtworkq.RtwqInvokeCallback
title: RtwqInvokeCallback function (rtworkq.h)
description: Invokes a callback method to complete an asynchronous operation. (RtwqInvokeCallback)
helpviewer_keywords: ["RtwqInvokeCallback","RtwqInvokeCallback function","base.rtwqinvokecallback","rtworkq/RtwqInvokeCallback"]
old-location: base\rtwqinvokecallback.htm
tech.root: backup
ms.assetid: ba1ac638-b21d-4a0e-8599-b572b5ef2fa6
ms.date: 12/05/2018
ms.keywords: RtwqInvokeCallback, RtwqInvokeCallback function, base.rtwqinvokecallback, rtworkq/RtwqInvokeCallback
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
 - RtwqInvokeCallback
 - rtworkq/RtwqInvokeCallback
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
 - RtwqInvokeCallback
---

# RtwqInvokeCallback function


## -description

Invokes a callback method to complete an asynchronous operation.

## -parameters

### -param result

The asynchronous result. To create this object, call <a href="/windows/desktop/api/rtworkq/nf-rtworkq-rtwqcreateasyncresult">RtwqCreateAsyncResult</a>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
