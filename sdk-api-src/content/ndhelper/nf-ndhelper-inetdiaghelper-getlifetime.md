---
UID: NF:ndhelper.INetDiagHelper.GetLifeTime
title: INetDiagHelper::GetLifeTime (ndhelper.h)
description: Retrieves the lifetime of the Helper Class Extension instance.
helpviewer_keywords: ["GetLifeTime","GetLifeTime method [NDF]","GetLifeTime method [NDF]","INetDiagHelper interface","INetDiagHelper interface [NDF]","GetLifeTime method","INetDiagHelper.GetLifeTime","INetDiagHelper::GetLifeTime","ndf.inetdiaghelpe_getlifetime","ndhelper/INetDiagHelper::GetLifeTime"]
old-location: ndf\inetdiaghelpe_getlifetime.htm
tech.root: NDF
ms.assetid: 0710b8d3-04d6-434f-9b0a-22049bf00ba0
ms.date: 12/05/2018
ms.keywords: GetLifeTime, GetLifeTime method [NDF], GetLifeTime method [NDF],INetDiagHelper interface, INetDiagHelper interface [NDF],GetLifeTime method, INetDiagHelper.GetLifeTime, INetDiagHelper::GetLifeTime, ndf.inetdiaghelpe_getlifetime, ndhelper/INetDiagHelper::GetLifeTime
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
 - INetDiagHelper::GetLifeTime
 - ndhelper/INetDiagHelper::GetLifeTime
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
 - INetDiagHelper.GetLifeTime
---

# INetDiagHelper::GetLifeTime


## -description

The <b>GetLifeTime</b> method retrieves the lifetime of the Helper Class Extension instance.

## -parameters

### -param pLifeTime [out]

A pointer to a <a href="/windows/desktop/api/ndattrib/ns-ndattrib-life_time">LIFE_TIME</a> structure.

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

Lifetime data is used to limit the time scope of a problem instance.  This is particularly useful when doing history-based diagnoses such as tracing and logging where it can be used in scoping down the diagnosis to events that occurred during the specified time interval.

For example, Windows Filtering Platform (WFP) helper classes use lifetime to determine  which filter blocked a packet by checking the trace log. By default, a lifetime of a helper class instance inherits the lifetime of its dependent helper class instance.

## -see-also

<a href="/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper">INetDiagHelper</a>