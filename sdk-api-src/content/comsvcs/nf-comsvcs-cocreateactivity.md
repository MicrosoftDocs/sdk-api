---
UID: NF:comsvcs.CoCreateActivity
title: CoCreateActivity function (comsvcs.h)
description: Creates an activity to do synchronous or asynchronous batch work that can use COM+ services without needing to create a COM+ component.
helpviewer_keywords: ["CoCreateActivity","CoCreateActivity function [COM+]","_cos_CoCreateActivity","comsvcs/CoCreateActivity","cos.cocreateactivity"]
old-location: cos\cocreateactivity.htm
tech.root: cos
ms.assetid: 3009eb4f-e3f3-497b-ba05-5b750d8a40d0
ms.date: 12/05/2018
ms.keywords: CoCreateActivity, CoCreateActivity function [COM+], _cos_CoCreateActivity, comsvcs/CoCreateActivity, cos.cocreateactivity
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
 - CoCreateActivity
 - comsvcs/CoCreateActivity
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
 - CoCreateActivity
---

# CoCreateActivity function


## -description

Creates an activity to do synchronous or asynchronous batch work that can use COM+ services without needing to create a COM+ component.

## -parameters

### -param pIUnknown [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the object, created from the <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> class, that contains the configuration information for the services to be used within the activity created by <b>CoCreateActivity</b>.

### -param riid [in]

The ID of the interface to be returned through the <i>ppObj</i> parameter. This parameter should always be IID_IServiceActivity so that a pointer to <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a> is returned.

### -param ppObj [out]

A pointer to the interface  of an activity object. The activity object is automatically created by the call to <b>CoCreateActivity</b>.

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
The thread pool configuration of the <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> object is invalid.

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

<b>CoCreateActivity</b> creates an activity object that is used to submit batch work to the COM+ system. The context associated with the activity is completely determined by the <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> object that is passed through the <i>pIUnknown</i> parameter.

<b>CoCreateActivity</b> enables applications to use COM+ services in their batch work without needing to create a component to use those services. In addition to reducing overhead by not requiring the creation of a component, using <b>CoCreateActivity</b> provides for a more efficient runtime environment because it allows the environment to support application-wide service configuration without needing to access information that is stored in the COM+ registration database (RegDB).

The batch work that is submitted through <b>CoCreateActivity</b> can be either synchronous or asynchronous and can run in either a single-threaded apartment (STA) or the multithreaded apartment (MTA). The threading model that is used is determined by the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicethreadpoolconfig">IServiceThreadPoolConfig</a> interface of the <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> object that is passed through the <i>pIUnknown</i> parameter.

<b>CoCreateActivity</b> returns a pointer to the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a> interface of the object that is created by the call to <b>CoCreateActivity</b>. By using the methods of <b>IServiceActivity</b>, you determine whether the batch work is done synchronously or asynchronously. The batch work itself is implemented through the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicecall">IServiceCall</a> interface.

## -see-also

<a href="/windows/desktop/cossdk/com--services-without-components">COM+ Services Without Components</a>



<a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicecall">IServiceCall</a>