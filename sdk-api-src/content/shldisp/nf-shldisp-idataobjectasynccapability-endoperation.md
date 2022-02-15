---
UID: NF:shldisp.IDataObjectAsyncCapability.EndOperation
title: IDataObjectAsyncCapability::EndOperation (shldisp.h)
description: Notifies the data object that the asynchronous data extraction has ended.
helpviewer_keywords: ["EndOperation","EndOperation method [Windows Shell]","EndOperation method [Windows Shell]","IDataObjectAsyncCapability interface","IDataObjectAsyncCapability interface [Windows Shell]","EndOperation method","IDataObjectAsyncCapability.EndOperation","IDataObjectAsyncCapability::EndOperation","shell.IDataObjectAsyncCapability_EndOperation","shldisp/IDataObjectAsyncCapability::EndOperation"]
old-location: shell\IDataObjectAsyncCapability_EndOperation.htm
tech.root: shell
ms.assetid: CF9D2A95-12AF-4538-882D-B391F2E087ED
ms.date: 12/05/2018
ms.keywords: EndOperation, EndOperation method [Windows Shell], EndOperation method [Windows Shell],IDataObjectAsyncCapability interface, IDataObjectAsyncCapability interface [Windows Shell],EndOperation method, IDataObjectAsyncCapability.EndOperation, IDataObjectAsyncCapability::EndOperation, shell.IDataObjectAsyncCapability_EndOperation, shldisp/IDataObjectAsyncCapability::EndOperation
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataObjectAsyncCapability::EndOperation
 - shldisp/IDataObjectAsyncCapability::EndOperation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDataObjectAsyncCapability.EndOperation
---

# IDataObjectAsyncCapability::EndOperation


## -description

Notifies the data object that the asynchronous data extraction has ended.

## -parameters

### -param hResult [in]

Type: <b>HRESULT</b>

Indicates the outcome of the data extraction. Set this value to S_OK if successful, or a COM error code otherwise.

### -param pbcReserved [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

Reserved. Set to <b>nullptr</b>.

### -param dwEffects [in]

Type: <b>DWORD</b>

A <a href="/windows/desktop/com/dropeffect-constants">DROPEFFECT</a> value that indicates the result of an optimized move. This should be the same value that would be passed to the data object as a CFSTR_PERFORMEDDROPEFFECT format with a normal data extraction operation.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>EndOperation</b> retrieves the <a href="/windows/desktop/api/shldisp/nn-shldisp-idataobjectasynccapability">IDataObjectAsyncCapability</a> pointer stored by <a href="/windows/desktop/api/shldisp/nf-shldisp-idataobjectasynccapability-setasyncmode">IDataObjectAsyncCapability::SetAsyncMode</a> and passes its parameter values to that interface's <b>IDataObjectAsyncCapability::EndOperation</b> method. <b>EndOperation</b> then releases the <b>IDataObjectAsyncCapability</b> pointer.

<b>EndOperation</b> is also responsible for any associated clean-up operations. When finished, <b>EndOperation</b> should notify the drop source through a private interface.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-idataobjectasynccapability">IDataObjectAsyncCapability</a>