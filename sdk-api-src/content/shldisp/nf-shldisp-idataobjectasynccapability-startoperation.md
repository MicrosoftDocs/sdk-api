---
UID: NF:shldisp.IDataObjectAsyncCapability.StartOperation
title: IDataObjectAsyncCapability::StartOperation (shldisp.h)
description: Called by a drop target to indicate that asynchronous data extraction is starting.
helpviewer_keywords: ["IDataObjectAsyncCapability interface [Windows Shell]","StartOperation method","IDataObjectAsyncCapability.StartOperation","IDataObjectAsyncCapability::StartOperation","StartOperation","StartOperation method [Windows Shell]","StartOperation method [Windows Shell]","IDataObjectAsyncCapability interface","shell.IDataObjectAsyncCapability_StartOperation","shldisp/IDataObjectAsyncCapability::StartOperation"]
old-location: shell\IDataObjectAsyncCapability_StartOperation.htm
tech.root: shell
ms.assetid: 84C1E709-ADFD-4c00-B767-C0DB4C30578A
ms.date: 12/05/2018
ms.keywords: IDataObjectAsyncCapability interface [Windows Shell],StartOperation method, IDataObjectAsyncCapability.StartOperation, IDataObjectAsyncCapability::StartOperation, StartOperation, StartOperation method [Windows Shell], StartOperation method [Windows Shell],IDataObjectAsyncCapability interface, shell.IDataObjectAsyncCapability_StartOperation, shldisp/IDataObjectAsyncCapability::StartOperation
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
 - IDataObjectAsyncCapability::StartOperation
 - shldisp/IDataObjectAsyncCapability::StartOperation
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
 - IDataObjectAsyncCapability.StartOperation
---

# IDataObjectAsyncCapability::StartOperation


## -description

Called by a drop target to indicate that asynchronous data extraction is starting.

## -parameters

### -param pbcReserved [in, optional]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a>*</b>

Reserved. Set this value to <b>nullptr</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The drop target calls this method to notify the data object that asynchronous data extraction is starting. The method should store this information so that it can be returned by <a href="/windows/desktop/api/shldisp/nf-shldisp-idataobjectasynccapability-inoperation">IDataObjectAsyncCapability::InOperation</a>. Once <b>StartOperation</b> has been called, the drop target returns the <a href="/windows/desktop/api/oleidl/nf-oleidl-idroptarget-drop">IDropTarget::Drop</a> call as it would for normal synchronous data extraction.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-idataobjectasynccapability">IDataObjectAsyncCapability</a>