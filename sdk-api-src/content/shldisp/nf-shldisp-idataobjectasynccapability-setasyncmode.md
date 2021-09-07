---
UID: NF:shldisp.IDataObjectAsyncCapability.SetAsyncMode
title: IDataObjectAsyncCapability::SetAsyncMode (shldisp.h)
description: Called by a drop source to specify whether the data object supports asynchronous data extraction.
helpviewer_keywords: ["IDataObjectAsyncCapability interface [Windows Shell]","SetAsyncMode method","IDataObjectAsyncCapability.SetAsyncMode","IDataObjectAsyncCapability::SetAsyncMode","SetAsyncMode","SetAsyncMode method [Windows Shell]","SetAsyncMode method [Windows Shell]","IDataObjectAsyncCapability interface","shell.IDataObjectAsyncCapability_SetAsyncMode","shldisp/IDataObjectAsyncCapability::SetAsyncMode"]
old-location: shell\IDataObjectAsyncCapability_SetAsyncMode.htm
tech.root: shell
ms.assetid: 97DCCA78-F25E-47de-8292-F0C6ED9DFD35
ms.date: 12/05/2018
ms.keywords: IDataObjectAsyncCapability interface [Windows Shell],SetAsyncMode method, IDataObjectAsyncCapability.SetAsyncMode, IDataObjectAsyncCapability::SetAsyncMode, SetAsyncMode, SetAsyncMode method [Windows Shell], SetAsyncMode method [Windows Shell],IDataObjectAsyncCapability interface, shell.IDataObjectAsyncCapability_SetAsyncMode, shldisp/IDataObjectAsyncCapability::SetAsyncMode
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
 - IDataObjectAsyncCapability::SetAsyncMode
 - shldisp/IDataObjectAsyncCapability::SetAsyncMode
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
 - IDataObjectAsyncCapability.SetAsyncMode
---

# IDataObjectAsyncCapability::SetAsyncMode


## -description

Called by a drop source to specify whether the data object supports asynchronous data extraction.

## -parameters

### -param fDoOpAsync [in]

Type: <b>BOOL</b>

<b>VARIANT_TRUE</b> if an asynchronous operation is supported; otherwise, <b>VARIANT_FALSE</b>. The default value is <b>VARIANT_FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called by the drop source to indicate that the data object supports asynchronous data extraction. Store the <i>fDoOpAsync</i> for later use by <a href="/windows/desktop/api/shldisp/nf-shldisp-idataobjectasynccapability-getasyncmode">IDataObjectAsyncCapability::GetAsyncMode</a>. The drop target determines whether asynchronous data extraction is supported by calling <b>IDataObjectAsyncCapability::GetAsyncMode</b> to retrieve the <i>fDoOpAsync</i> value.

If <i>fDoOpAsync</i> is set to <b>VARIANT_TRUE</b>, <b>SetAsyncMode</b> must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IDataObjectAsyncCapability::AddRef</a>, and store the interface pointer for use by <a href="/windows/desktop/api/shldisp/nf-shldisp-idataobjectasynccapability-endoperation">IDataObjectAsyncCapability::EndOperation</a>.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-idataobjectasynccapability">IDataObjectAsyncCapability</a>