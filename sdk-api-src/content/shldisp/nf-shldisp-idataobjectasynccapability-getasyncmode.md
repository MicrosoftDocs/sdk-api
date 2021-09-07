---
UID: NF:shldisp.IDataObjectAsyncCapability.GetAsyncMode
title: IDataObjectAsyncCapability::GetAsyncMode (shldisp.h)
description: Called by a drop target to determine whether the data object supports asynchronous data extraction.
helpviewer_keywords: ["GetAsyncMode","GetAsyncMode method [Windows Shell]","GetAsyncMode method [Windows Shell]","IDataObjectAsyncCapability interface","IDataObjectAsyncCapability interface [Windows Shell]","GetAsyncMode method","IDataObjectAsyncCapability.GetAsyncMode","IDataObjectAsyncCapability::GetAsyncMode","shell.IDataObjectAsyncCapability_GetAsyncMode","shldisp/IDataObjectAsyncCapability::GetAsyncMode"]
old-location: shell\IDataObjectAsyncCapability_GetAsyncMode.htm
tech.root: shell
ms.assetid: 0B7A4299-4D19-4c5a-99A5-9568F4D58061
ms.date: 12/05/2018
ms.keywords: GetAsyncMode, GetAsyncMode method [Windows Shell], GetAsyncMode method [Windows Shell],IDataObjectAsyncCapability interface, IDataObjectAsyncCapability interface [Windows Shell],GetAsyncMode method, IDataObjectAsyncCapability.GetAsyncMode, IDataObjectAsyncCapability::GetAsyncMode, shell.IDataObjectAsyncCapability_GetAsyncMode, shldisp/IDataObjectAsyncCapability::GetAsyncMode
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
 - IDataObjectAsyncCapability::GetAsyncMode
 - shldisp/IDataObjectAsyncCapability::GetAsyncMode
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
 - IDataObjectAsyncCapability.GetAsyncMode
---

# IDataObjectAsyncCapability::GetAsyncMode


## -description

Called by a drop target to determine whether the data object supports asynchronous data extraction.

## -parameters

### -param pfIsOpAsync [out]

Type: <b>BOOL*</b>

<b>VARIANT_TRUE</b> if an asynchronous operation is supported; otherwise, <b>VARIANT_FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The purpose of this method is to give the drop target the value of the <a href="/windows/desktop/api/shldisp/nf-shldisp-idataobjectasynccapability-setasyncmode">IDataObjectAsyncCapability::SetAsyncMode</a> method's <i>fDoOpAsync</i> parameter. This parameter is set to <b>VARIANT_FALSE</b> by default. If the data object supports asynchronous data extraction, it must call <b>IDataObjectAsyncCapability::SetAsyncMode</b> and set <i>fDoOpAsync</i> to <b>VARIANT_TRUE</b>.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-idataobjectasynccapability">IDataObjectAsyncCapability</a>