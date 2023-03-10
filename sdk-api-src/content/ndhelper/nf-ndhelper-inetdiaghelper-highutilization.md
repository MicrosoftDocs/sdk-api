---
UID: NF:ndhelper.INetDiagHelper.HighUtilization
title: INetDiagHelper::HighUtilization (ndhelper.h)
description: Check whether the corresponding component is highly utilized.
helpviewer_keywords: ["HighUtilization","HighUtilization method [NDF]","HighUtilization method [NDF]","INetDiagHelper interface","INetDiagHelper interface [NDF]","HighUtilization method","INetDiagHelper.HighUtilization","INetDiagHelper::HighUtilization","ndf.inetdiaghelpe_highutilization","ndhelper/INetDiagHelper::HighUtilization"]
old-location: ndf\inetdiaghelpe_highutilization.htm
tech.root: NDF
ms.assetid: 4a555683-f7fd-43a4-808a-60579723293c
ms.date: 12/05/2018
ms.keywords: HighUtilization, HighUtilization method [NDF], HighUtilization method [NDF],INetDiagHelper interface, INetDiagHelper interface [NDF],HighUtilization method, INetDiagHelper.HighUtilization, INetDiagHelper::HighUtilization, ndf.inetdiaghelpe_highutilization, ndhelper/INetDiagHelper::HighUtilization
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
 - INetDiagHelper::HighUtilization
 - ndhelper/INetDiagHelper::HighUtilization
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
 - INetDiagHelper.HighUtilization
---

# INetDiagHelper::HighUtilization


## -description

The <b>HighUtilization</b> method enables the Helper Class Extension to check whether the corresponding component is highly utilized.

## -parameters

### -param pwszInstanceDescription [in]

A pointer to a null-terminated string containing the user-friendly description of the information being diagnosed.  For example, if a class were to diagnosis a connectivity issue with an IP address, the <i>pwszInstanceDescription</i> parameter would contain the host name.

### -param ppwszDescription [out]

A pointer to a null-terminated string containing the description of high utilization diagnosis result.

### -param pDeferredTime [out]

A pointer to the time, in seconds, to be deferred if the diagnosis cannot be started immediately. This is used when the <i>pStatus</i> parameter is set to <b>DS_DEFERRED</b>.

### -param pStatus [out]

A pointer to the <a href="/windows/desktop/api/ndhelper/ne-ndhelper-diagnosis_status">DIAGNOSIS_STATUS</a> that is returned from the diagnosis.

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