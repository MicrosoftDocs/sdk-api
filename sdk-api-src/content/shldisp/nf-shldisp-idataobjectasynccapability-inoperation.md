---
UID: NF:shldisp.IDataObjectAsyncCapability.InOperation
title: IDataObjectAsyncCapability::InOperation (shldisp.h)
description: Called by the drop source to determine whether the target is extracting data asynchronously.helpviewer_keywords: ["IDataObjectAsyncCapability interface [Windows Shell]","InOperation method","IDataObjectAsyncCapability.InOperation","IDataObjectAsyncCapability::InOperation","InOperation","InOperation method [Windows Shell]","InOperation method [Windows Shell]","IDataObjectAsyncCapability interface","shell.IDataObjectAsyncCapability_InOperation","shldisp/IDataObjectAsyncCapability::InOperation"]
old-location: shell\IDataObjectAsyncCapability_InOperation.htm
tech.root: shell
ms.assetid: 858EB8C4-88AB-40a3-B4FC-CCD19235CE55
ms.date: 12/05/2018
ms.keywords: IDataObjectAsyncCapability interface [Windows Shell],InOperation method, IDataObjectAsyncCapability.InOperation, IDataObjectAsyncCapability::InOperation, InOperation, InOperation method [Windows Shell], InOperation method [Windows Shell],IDataObjectAsyncCapability interface, shell.IDataObjectAsyncCapability_InOperation, shldisp/IDataObjectAsyncCapability::InOperation
f1_keywords:
- shldisp/IDataObjectAsyncCapability.InOperation
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- IDataObjectAsyncCapability.InOperation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataObjectAsyncCapability::InOperation


## -description


Called by the drop source to determine whether the target is extracting data asynchronously.


## -parameters




### -param pfInAsyncOp [out]

Type: <b>BOOL*</b>

<b>VARIANT_TRUE</b> if data extraction is being handled asynchronously; otherwise, <b>VARIANT_FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called by the drop source after <a href="https://docs.microsoft.com/windows/desktop/api/ole2/nf-ole2-dodragdrop">DoDragDrop</a> returns. The <i>pfInAsyncOp</i> parameter should be set to <b>VARIANT_TRUE</b> only if the drop target has called <a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-idataobjectasynccapability-startoperation">IDataObjectAsyncCapability::StartOperation</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-idataobjectasynccapability">IDataObjectAsyncCapability</a>
 

 

