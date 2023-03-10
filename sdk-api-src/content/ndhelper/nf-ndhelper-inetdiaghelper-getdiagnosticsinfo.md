---
UID: NF:ndhelper.INetDiagHelper.GetDiagnosticsInfo
title: INetDiagHelper::GetDiagnosticsInfo (ndhelper.h)
description: Enables the Helper Class Extension instance to provide an estimate.
helpviewer_keywords: ["GetDiagnosticsInfo","GetDiagnosticsInfo method [NDF]","GetDiagnosticsInfo method [NDF]","INetDiagHelper interface","INetDiagHelper interface [NDF]","GetDiagnosticsInfo method","INetDiagHelper.GetDiagnosticsInfo","INetDiagHelper::GetDiagnosticsInfo","ndf.inetdiaghelpe_getdiagnosticsinfo","ndhelper/INetDiagHelper::GetDiagnosticsInfo"]
old-location: ndf\inetdiaghelpe_getdiagnosticsinfo.htm
tech.root: NDF
ms.assetid: bc162b1b-a22e-4ee3-96a6-c2eecc13e479
ms.date: 12/05/2018
ms.keywords: GetDiagnosticsInfo, GetDiagnosticsInfo method [NDF], GetDiagnosticsInfo method [NDF],INetDiagHelper interface, INetDiagHelper interface [NDF],GetDiagnosticsInfo method, INetDiagHelper.GetDiagnosticsInfo, INetDiagHelper::GetDiagnosticsInfo, ndf.inetdiaghelpe_getdiagnosticsinfo, ndhelper/INetDiagHelper::GetDiagnosticsInfo
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
 - INetDiagHelper::GetDiagnosticsInfo
 - ndhelper/INetDiagHelper::GetDiagnosticsInfo
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
 - INetDiagHelper.GetDiagnosticsInfo
---

# INetDiagHelper::GetDiagnosticsInfo


## -description

The <b>GetDiagnosticsInfo</b> method enables the Helper Class Extension instance to provide an estimate of how long the diagnosis may take.

## -parameters

### -param ppInfo [out]

A pointer to a pointer to a <a href="/windows/desktop/api/ndhelper/ns-ndhelper-diagnosticsinfo">DiagnosticsInfo</a> structure.

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

The GetDiagnosticsInfo method is required when building a Helper Class Extension.

## -see-also

<a href="/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper">INetDiagHelper</a>