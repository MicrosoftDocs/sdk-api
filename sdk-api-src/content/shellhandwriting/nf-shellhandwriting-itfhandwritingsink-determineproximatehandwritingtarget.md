---
UID: NF:shellhandwriting.ITfHandwritingSink.DetermineProximateHandwritingTarget
tech.root: input_ink
title: ITfHandwritingSink::DetermineProximateHandwritingTarget
ms.date: 11/14/2023
targetos: Windows
description: 
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: shellhandwriting.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - shellhandwriting.h
api_name:
 - ITfHandwritingSink::DetermineProximateHandwritingTarget
f1_keywords:
 - ITfHandwritingSink::DetermineProximateHandwritingTarget
 - shellhandwriting/ITfHandwritingSink::DetermineProximateHandwritingTarget
dev_langs:
 - c++
helpviewer_keywords:
 - DetermineProximateHandwritingTarget
---

# DetermineProximateHandwritingTarget function

## -description

Determines whether an edit control exists (or might exist in a dynamic user experience) proximate to the the pointer input.

## -parameters

### -param determineProximateHandwritingTargetArgs [in]

[ITfDetermineProximateHandwritingTargetArgs interface](nn-shellhandwriting-itfdetermineproximatehandwritingtargetargs.md)

## -returns

If the method succeeds, it returns **S_OK**. If it fails, it returns an **HRESULT** error code.

## -remarks

This method is called when the system has detected pen input indicating a handwriting experience might be appropriate.

Secondary clients (frameworks) are called only if a primary client (application) does not provide a response to the callback.

Secondary clients are called in reverse order of registration until either S_OK or TF_S_ASYNC response is received from the callback. An example of a secondary client could be a control that provides custom handwriting logic regardless of the application instantiating the control. Secondary clients can register by obtaining an [ITfSource](../msctf/nn-msctf-itfsource.md) interface from an [ITfThreadMgr](../msctf/nn-msctf-itfthreadmgr.md) instance and then calling [AdviseSink](../msctf/nf-msctf-itfsource-advisesink.md) with an [ITfHandwritingSink interface](nn-shellhandwriting-itfhandwritingsink.md) object.

If neither primary or secondary clients allow the system to continue with the next client (or fall back to User Interface Automation (UIA)), they should return E_INVALIDARG.

If a client responds with TF_USE_SYSTEM_DEFAULT, and returns S_OK, subsequent clients will be skipped and the system will use its default UIA-based determination logic.

## -see-also

