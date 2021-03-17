---
UID: NF:ndhelper.INetDiagHelper.LowHealth
title: INetDiagHelper::LowHealth (ndhelper.h)
description: Check whether the component being diagnosed is healthy.
helpviewer_keywords: ["INetDiagHelper interface [NDF]","LowHealth method","INetDiagHelper.LowHealth","INetDiagHelper::LowHealth","LowHealth","LowHealth method [NDF]","LowHealth method [NDF]","INetDiagHelper interface","ndf.inetdiaghelpe_lowhealth","ndhelper/INetDiagHelper::LowHealth"]
old-location: ndf\inetdiaghelpe_lowhealth.htm
tech.root: NDF
ms.assetid: 623de90f-c2dc-4879-9baf-4051d2d3691c
ms.date: 12/05/2018
ms.keywords: INetDiagHelper interface [NDF],LowHealth method, INetDiagHelper.LowHealth, INetDiagHelper::LowHealth, LowHealth, LowHealth method [NDF], LowHealth method [NDF],INetDiagHelper interface, ndf.inetdiaghelpe_lowhealth, ndhelper/INetDiagHelper::LowHealth
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
 - INetDiagHelper::LowHealth
 - ndhelper/INetDiagHelper::LowHealth
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
 - INetDiagHelper.LowHealth
---

# INetDiagHelper::LowHealth


## -description

The <b>LowHealth</b> method enables the Helper Class Extension to check whether the component being diagnosed is healthy.

## -parameters

### -param pwszInstanceDescription [in]

A pointer to a null-terminated string containing the user-friendly description of the information being diagnosed.  For example, if a class were to diagnosis a connectivity issue with an IP address, the <i>pwszInstanceDescription</i> parameter would contain the host name.

### -param ppwszDescription [out]

A pointer to a null-terminated string containing the description of the issue found if the component is found to be unhealthy.

### -param pDeferredTime [out]

A pointer to the time, in seconds, to be deferred if the diagnosis cannot be started immediately.  This is used when the <i>pStatus</i> parameter is set to <b>DS_DEFERRED</b>.

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

The LowHealth method is required when building a Helper Class Extension.

If LowHealth returns <b>DS_CONFIRMED</b>, <i>ppwszDescription</i> will also contain a user-friendly description of the diagnosis result. The out parameter <i>pDeferredTime</i> contains the number of seconds this diagnosis needs to be deferred if pStatus returns <b>DS_DEFERRED</b>.

When LowHealth is confirmed, it may also optionally generate hypotheses in the <a href="/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getlowerhypotheses">GetLowerHypotheses</a> method for other helper classes if the problem may be caused by other components.  If not confirmed, NDF may further diagnose the problem by calling <a href="/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization">HighUtilization</a>.

LowHealth may also return <b>DS_INDETERMINATE</b> if it is unable to diagnose the problem, but cannot confirm that the component is healthy. In this case, NDF will treat it as <b>DS_CONFIRMED</b> if none of the other hypotheses are confirmed.

## -see-also

<a href="/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper">INetDiagHelper</a>