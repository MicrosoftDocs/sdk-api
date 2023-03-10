---
UID: NF:ndhelper.INetDiagHelper.GetLowerHypotheses
title: INetDiagHelper::GetLowerHypotheses (ndhelper.h)
description: Generate hypotheses for possible causes of low health in the local components.
helpviewer_keywords: ["GetLowerHypotheses","GetLowerHypotheses method [NDF]","GetLowerHypotheses method [NDF]","INetDiagHelper interface","INetDiagHelper interface [NDF]","GetLowerHypotheses method","INetDiagHelper.GetLowerHypotheses","INetDiagHelper::GetLowerHypotheses","ndf.inetdiaghelpe_getlowerhypotheses","ndhelper/INetDiagHelper::GetLowerHypotheses"]
old-location: ndf\inetdiaghelpe_getlowerhypotheses.htm
tech.root: NDF
ms.assetid: d17f5241-6efb-45a7-b355-8343e48b3261
ms.date: 12/05/2018
ms.keywords: GetLowerHypotheses, GetLowerHypotheses method [NDF], GetLowerHypotheses method [NDF],INetDiagHelper interface, INetDiagHelper interface [NDF],GetLowerHypotheses method, INetDiagHelper.GetLowerHypotheses, INetDiagHelper::GetLowerHypotheses, ndf.inetdiaghelpe_getlowerhypotheses, ndhelper/INetDiagHelper::GetLowerHypotheses
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
 - INetDiagHelper::GetLowerHypotheses
 - ndhelper/INetDiagHelper::GetLowerHypotheses
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
 - INetDiagHelper.GetLowerHypotheses
---

# INetDiagHelper::GetLowerHypotheses


## -description

The <b>GetLowerHypotheses</b> method asks the Helper Class Extension to generate hypotheses for possible causes of low health  in the local components that depend on it.

## -parameters

### -param pcelt [out]

A pointer to a count of elements in the <b>HYPOTHESIS</b> array.

### -param pprgHypotheses [out]

A pointer to a <a href="/windows/desktop/api/ndhelper/ns-ndhelper-hypothesis">HYPOTHESIS</a> array.

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