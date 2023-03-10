---
UID: NF:ndhelper.INetDiagHelper.Validate
title: INetDiagHelper::Validate (ndhelper.h)
description: Called by NDF after a repair is successfully completed.
helpviewer_keywords: ["INetDiagHelper interface [NDF]","Validate method","INetDiagHelper.Validate","INetDiagHelper::Validate","Validate","Validate method [NDF]","Validate method [NDF]","INetDiagHelper interface","ndf.inetdiaghelpe_validate","ndhelper/INetDiagHelper::Validate"]
old-location: ndf\inetdiaghelpe_validate.htm
tech.root: NDF
ms.assetid: 2faab163-5684-4b10-b62d-7e22d5b789a8
ms.date: 12/05/2018
ms.keywords: INetDiagHelper interface [NDF],Validate method, INetDiagHelper.Validate, INetDiagHelper::Validate, Validate, Validate method [NDF], Validate method [NDF],INetDiagHelper interface, ndf.inetdiaghelpe_validate, ndhelper/INetDiagHelper::Validate
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
 - INetDiagHelper::Validate
 - ndhelper/INetDiagHelper::Validate
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
 - INetDiagHelper.Validate
---

# INetDiagHelper::Validate


## -description

The <b>Validate</b> method is called by NDF after a repair is successfully completed in order to validate that a previously diagnosed problem has been fixed.

## -parameters

### -param problem [in]

The <a href="/windows/desktop/api/ndhelper/ne-ndhelper-problem_type">PROBLEM_TYPE</a> that the helper class has previously diagnosed.

### -param pDeferredTime [out]

A pointer to the time to be deferred, in seconds, if the diagnosis cannot be started immediately. This is used only when the pStatus member is set to <b>DS_DEFERRED</b>.

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

This method only returns an error code if it encounters failures that impede validation. If necessary, the <i>pStatus</i> parameter is the expected way to communicate that the component is still in low health. <b>DS_REJECTED</b> is used to indicate that the issue has been resolved.

## -see-also

<a href="/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper">INetDiagHelper</a>