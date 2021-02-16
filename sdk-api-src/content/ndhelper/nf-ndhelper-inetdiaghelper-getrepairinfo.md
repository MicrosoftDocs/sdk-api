---
UID: NF:ndhelper.INetDiagHelper.GetRepairInfo
title: INetDiagHelper::GetRepairInfo (ndhelper.h)
description: Retrieves the repair information that the Helper Class Extension has for a given problem type.
helpviewer_keywords: ["GetRepairInfo","GetRepairInfo method [NDF]","GetRepairInfo method [NDF]","INetDiagHelper interface","INetDiagHelper interface [NDF]","GetRepairInfo method","INetDiagHelper.GetRepairInfo","INetDiagHelper::GetRepairInfo","ndf.inetdiaghelpe_getrepairinfo","ndhelper/INetDiagHelper::GetRepairInfo"]
old-location: ndf\inetdiaghelpe_getrepairinfo.htm
tech.root: NDF
ms.assetid: a14b1f61-1ac7-4ee7-ad82-e0821f43a17d
ms.date: 12/05/2018
ms.keywords: GetRepairInfo, GetRepairInfo method [NDF], GetRepairInfo method [NDF],INetDiagHelper interface, INetDiagHelper interface [NDF],GetRepairInfo method, INetDiagHelper.GetRepairInfo, INetDiagHelper::GetRepairInfo, ndf.inetdiaghelpe_getrepairinfo, ndhelper/INetDiagHelper::GetRepairInfo
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
 - INetDiagHelper::GetRepairInfo
 - ndhelper/INetDiagHelper::GetRepairInfo
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
 - INetDiagHelper.GetRepairInfo
---

# INetDiagHelper::GetRepairInfo


## -description

The <b>GetRepairInfo</b> method retrieves the repair information that the Helper Class Extension has for a given problem type.

## -parameters

### -param problem [in]

A <a href="/windows/desktop/api/ndhelper/ne-ndhelper-problem_type">PROBLEM_TYPE</a> value that specifies the problem type that the helper class has previously diagnosed.

### -param pcelt [out]

A pointer to a count of elements in the <b>RepairInfo</b> array.

### -param ppInfo [out]

A pointer to an array of <a href="/windows/desktop/api/ndattrib/ns-ndattrib-repairinfo">RepairInfo</a> structures.

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