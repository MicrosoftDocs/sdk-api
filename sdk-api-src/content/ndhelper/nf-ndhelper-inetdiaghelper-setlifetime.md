---
UID: NF:ndhelper.INetDiagHelper.SetLifeTime
title: INetDiagHelper::SetLifeTime (ndhelper.h)
description: The Helper Class Extension can limit its diagnosis to events within that time period.
helpviewer_keywords: ["INetDiagHelper interface [NDF]","SetLifeTime method","INetDiagHelper.SetLifeTime","INetDiagHelper::SetLifeTime","SetLifeTime","SetLifeTime method [NDF]","SetLifeTime method [NDF]","INetDiagHelper interface","ndf.inetdiaghelpe_setlifetime","ndhelper/INetDiagHelper::SetLifeTime"]
old-location: ndf\inetdiaghelpe_setlifetime.htm
tech.root: NDF
ms.assetid: a211c885-364f-4ba5-a4c9-88a87b30cdc7
ms.date: 12/05/2018
ms.keywords: INetDiagHelper interface [NDF],SetLifeTime method, INetDiagHelper.SetLifeTime, INetDiagHelper::SetLifeTime, SetLifeTime, SetLifeTime method [NDF], SetLifeTime method [NDF],INetDiagHelper interface, ndf.inetdiaghelpe_setlifetime, ndhelper/INetDiagHelper::SetLifeTime
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
 - INetDiagHelper::SetLifeTime
 - ndhelper/INetDiagHelper::SetLifeTime
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
 - INetDiagHelper.SetLifeTime
---

# INetDiagHelper::SetLifeTime


## -description

The <b>SetLifeTime</b> method is called by NDF to set the start and end time of interest to diagnostics so that the Helper Class Extension can limit its diagnosis to events within that time period.

## -parameters

### -param lifeTime [in]

A <a href="/windows/desktop/api/ndattrib/ns-ndattrib-life_time">LIFE_TIME</a> structure.

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