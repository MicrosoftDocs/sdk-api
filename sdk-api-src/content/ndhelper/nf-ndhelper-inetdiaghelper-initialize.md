---
UID: NF:ndhelper.INetDiagHelper.Initialize
title: INetDiagHelper::Initialize (ndhelper.h)
description: The Initialize method passes in attributes to the Helper Class Extension from the hypothesis. The helper class should store these parameters for use in the main diagnostics functions. This method must be called before any diagnostics function.
helpviewer_keywords: ["INetDiagHelper interface [NDF]","Initialize method","INetDiagHelper.Initialize","INetDiagHelper::Initialize","Initialize","Initialize method [NDF]","Initialize method [NDF]","INetDiagHelper interface","ndf.inetdiaghelpe_initialize","ndhelper/INetDiagHelper::Initialize"]
old-location: ndf\inetdiaghelpe_initialize.htm
tech.root: NDF
ms.assetid: 32003720-ca59-4203-a78c-9e40c626c9f8
ms.date: 12/05/2018
ms.keywords: INetDiagHelper interface [NDF],Initialize method, INetDiagHelper.Initialize, INetDiagHelper::Initialize, Initialize, Initialize method [NDF], Initialize method [NDF],INetDiagHelper interface, ndf.inetdiaghelpe_initialize, ndhelper/INetDiagHelper::Initialize
req.header: ndhelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetDiagHelper::Initialize
 - ndhelper/INetDiagHelper::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ndhelper.h
api_name:
 - INetDiagHelper.Initialize
---

# INetDiagHelper::Initialize


## -description

The <b>Initialize</b> method passes in attributes to the Helper Class Extension from the hypothesis.  The helper class should store these parameters for use in the main diagnostics functions.  This method must be called before any diagnostics function.

## -parameters

### -param celt [in]

A pointer to a count of elements in <b>HELPER_ATTRIBUTE</b> array.

### -param rgAttributes

A reference to the <a href="/windows/desktop/api/ndattrib/ns-ndattrib-helper_attribute">HELPER_ATTRIBUTE</a> array.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters has not been provided correctly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges to perform the diagnosis or repair operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The diagnosis or repair operation has been canceled.

</td>
</tr>
</table>
 

Helper Class Extensions may return HRESULTS that are specific to the failures encountered in the function.

## -remarks

The Initialize method is required when building a Helper Class Extension.

## -see-also

<a href="/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper">INetDiagHelper</a>