---
UID: NF:comsvcs.CoEnterServiceDomain
title: CoEnterServiceDomain function (comsvcs.h)
description: Used to enter code that can then use COM+ services.
helpviewer_keywords: ["CoEnterServiceDomain","CoEnterServiceDomain function [COM+]","_cos_CoEnterServiceDomain","comsvcs/CoEnterServiceDomain","cos.coenterservicedomain"]
old-location: cos\coenterservicedomain.htm
tech.root: cos
ms.assetid: 84640b3b-1f43-4bec-abf6-c295cfb3da8b
ms.date: 12/05/2018
ms.keywords: CoEnterServiceDomain, CoEnterServiceDomain function [COM+], _cos_CoEnterServiceDomain, comsvcs/CoEnterServiceDomain, cos.coenterservicedomain
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: ComSvcs.lib
req.dll: ComSvcs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoEnterServiceDomain
 - comsvcs/CoEnterServiceDomain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComSvcs.dll
api_name:
 - CoEnterServiceDomain
---

# CoEnterServiceDomain function


## -description

Used to enter code that can then use COM+ services.

## -parameters

### -param pConfigObject [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the object, created from the <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> class, that contains the configuration information for the services to be used within the enclosed code.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_FAIL, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_SXS_CONFIG</b></dt>
</dl>
</td>
<td width="60%">
The side-by-side assembly configuration of the <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> object is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_THREADPOOL_CONFIG</b></dt>
</dl>
</td>
<td width="60%">
The thread pool configuration of the <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> object is invalid. The thread apartment model cannot be reconfigured by calling <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_TRACKER_CONFIG</b></dt>
</dl>
</td>
<td width="60%">
The tracker configuration of the <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> object is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_PARTITION_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have access permissions for the COM+ partition.

</td>
</tr>
</table>

## -remarks

Code that is enclosed between calls to <b>CoEnterServiceDomain</b> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a> runs in its own context and behaves as though it were a method that is called on an object created within the context. <b>CoEnterServiceDomain</b> cannot switch to a different apartment model, so the enclosed code runs in the caller's apartment and on the caller's thread. It is an error to try to change the apartment model through the <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> object when calling <b>CoEnterServiceDomain</b>.

<b>CoEnterServiceDomain</b> first creates a context that is configured as specified by the <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> object that is passed as the <i>pConfigObject</i> parameter. Policies on both the client and server sides are then triggered as if a method call had occurred. The new context is then pushed onto a context stack and becomes the current context.

Because of their efficient design and because no thread marshaling is involved, using <b>CoEnterServiceDomain</b> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a> involves significantly reduced overhead as compared to an equivalent method call.

<b>CoEnterServiceDomain</b> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a> are particularly useful in applications, which can use these functions to access COM+ services without needing to create a component to do so.



The <b>CoEnterServiceDomain</b> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a> pairs can be nested.

## -see-also

<a href="/windows/desktop/cossdk/com--services-without-components">COM+ Services Without Components</a>



<a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a>