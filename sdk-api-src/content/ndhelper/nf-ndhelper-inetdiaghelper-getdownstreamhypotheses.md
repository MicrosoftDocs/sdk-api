---
UID: NF:ndhelper.INetDiagHelper.GetDownStreamHypotheses
title: INetDiagHelper::GetDownStreamHypotheses (ndhelper.h)
description: Asks the Helper Class Extension to generate hypotheses.
helpviewer_keywords: ["GetDownStreamHypotheses","GetDownStreamHypotheses method [NDF]","GetDownStreamHypotheses method [NDF]","INetDiagHelper interface","INetDiagHelper interface [NDF]","GetDownStreamHypotheses method","INetDiagHelper.GetDownStreamHypotheses","INetDiagHelper::GetDownStreamHypotheses","ndf.inetdiaghelpe_getdownstreamhypotheses","ndhelper/INetDiagHelper::GetDownStreamHypotheses"]
old-location: ndf\inetdiaghelpe_getdownstreamhypotheses.htm
tech.root: NDF
ms.assetid: ac26fbb5-d30f-4b1f-b432-043a07bfa853
ms.date: 12/05/2018
ms.keywords: GetDownStreamHypotheses, GetDownStreamHypotheses method [NDF], GetDownStreamHypotheses method [NDF],INetDiagHelper interface, INetDiagHelper interface [NDF],GetDownStreamHypotheses method, INetDiagHelper.GetDownStreamHypotheses, INetDiagHelper::GetDownStreamHypotheses, ndf.inetdiaghelpe_getdownstreamhypotheses, ndhelper/INetDiagHelper::GetDownStreamHypotheses
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
 - INetDiagHelper::GetDownStreamHypotheses
 - ndhelper/INetDiagHelper::GetDownStreamHypotheses
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
 - INetDiagHelper.GetDownStreamHypotheses
---

# INetDiagHelper::GetDownStreamHypotheses


## -description

The <b>GetDownStreamHypotheses</b> method asks the Helper Class Extension to generate hypotheses for possible causes of low health in the downstream network components it depends on.

## -parameters

### -param pcelt [out]

A pointer to a count of elements in the HYPOTHESIS array.

### -param pprgHypotheses [out]

A pointer to an array of <a href="/windows/desktop/api/ndhelper/ns-ndhelper-hypothesis">HYPOTHESIS</a> structures.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This optional method is not implemented.

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

This method is not required when building a Helper Class Extension.

## -see-also

<a href="/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper">INetDiagHelper</a>