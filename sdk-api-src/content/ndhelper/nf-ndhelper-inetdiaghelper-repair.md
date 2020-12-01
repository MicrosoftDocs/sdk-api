---
UID: NF:ndhelper.INetDiagHelper.Repair
title: INetDiagHelper::Repair (ndhelper.h)
description: Performs a repair specified by the input parameter.
helpviewer_keywords: ["INetDiagHelper interface [NDF]","Repair method","INetDiagHelper.Repair","INetDiagHelper::Repair","Repair","Repair method [NDF]","Repair method [NDF]","INetDiagHelper interface","ndf.inetdiaghelpe_repair","ndhelper/INetDiagHelper::Repair"]
old-location: ndf\inetdiaghelpe_repair.htm
tech.root: NDF
ms.assetid: 1892cbc8-01fd-4536-b29e-de733b0f6732
ms.date: 12/05/2018
ms.keywords: INetDiagHelper interface [NDF],Repair method, INetDiagHelper.Repair, INetDiagHelper::Repair, Repair, Repair method [NDF], Repair method [NDF],INetDiagHelper interface, ndf.inetdiaghelpe_repair, ndhelper/INetDiagHelper::Repair
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
 - INetDiagHelper::Repair
 - ndhelper/INetDiagHelper::Repair
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
 - INetDiagHelper.Repair
---

# INetDiagHelper::Repair


## -description

The <b>Repair</b> method performs a repair specified by the input parameter.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/desktop/api/ndattrib/ns-ndattrib-repairinfo">RepairInfo</a> structure.

### -param pDeferredTime [out]

A pointer to the time, in seconds, to be deferred if the repair cannot be started immediately. This is only valid when the pStatus parameter is set to <b>DS_DEFERRED</b>.

### -param pStatus [out]

A pointer to the <a href="/windows/desktop/api/ndhelper/ne-ndhelper-repair_status">REPAIR_STATUS</a> that is returned from the repair.

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