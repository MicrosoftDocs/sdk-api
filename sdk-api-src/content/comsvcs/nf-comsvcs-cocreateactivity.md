---
UID: NF:comsvcs.CoCreateActivity
title: CoCreateActivity function
author: windows-sdk-content
description: Creates an activity to do synchronous or asynchronous batch work that can use COM+ services without needing to create a COM+ component.
old-location: cos\cocreateactivity.htm
old-project: cossdk
ms.assetid: 3009eb4f-e3f3-497b-ba05-5b750d8a40d0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CoCreateActivity, CoCreateActivity function [COM+], _cos_CoCreateActivity, comsvcs/CoCreateActivity, cos.cocreateactivity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComSvcs.dll
api_name:
 - CoCreateActivity
product: Windows
targetos: Windows
req.lib: ComSvcs.lib
req.dll: ComSvcs.dll
req.irql: 
---

# CoCreateActivity function


## -description


Creates an activity to do synchronous or asynchronous batch work that can use COM+ services without needing to create a COM+ component.


## -parameters




### -param pIUnknown [in]

A pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the object, created from the <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> class, that contains the configuration information for the services to be used within the activity created by <b>CoCreateActivity</b>.


### -param riid [in]

The ID of the interface to be returned through the <i>ppObj</i> parameter. This parameter should always be IID_IServiceActivity so that a pointer to <a href="https://msdn.microsoft.com/005bf0ec-f5a7-41a3-85b3-07f79f26af27">IServiceActivity</a> is returned.


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
The side-by-side assembly configuration of the <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> object is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_THREADPOOL_CONFIG</b></dt>
</dl>
</td>
<td width="60%">
The thread pool configuration of the <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> object is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_TRACKER_CONFIG</b></dt>
</dl>
</td>
<td width="60%">
The tracker configuration of the <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> object is invalid.

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



<b>CoCreateActivity</b> creates an activity object that is used to submit batch work to the COM+ system. The context associated with the activity is completely determined by the <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> object that is passed through the <i>pIUnknown</i> parameter.

<b>CoCreateActivity</b> enables applications to use COM+ services in their batch work without needing to create a component to use those services. In addition to reducing overhead by not requiring the creation of a component, using <b>CoCreateActivity</b> provides for a more efficient runtime environment because it allows the environment to support application-wide service configuration without needing to access information that is stored in the COM+ registration database (RegDB).

The batch work that is submitted through <b>CoCreateActivity</b> can be either synchronous or asynchronous and can run in either a single-threaded apartment (STA) or the multithreaded apartment (MTA). The threading model that is used is determined by the <a href="https://msdn.microsoft.com/89c04fef-c6a0-4d73-a25a-a70b4b0f0bcf">IServiceThreadPoolConfig</a> interface of the <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> object that is passed through the <i>pIUnknown</i> parameter.

<b>CoCreateActivity</b> returns a pointer to the <a href="https://msdn.microsoft.com/005bf0ec-f5a7-41a3-85b3-07f79f26af27">IServiceActivity</a> interface of the object that is created by the call to <b>CoCreateActivity</b>. By using the methods of <b>IServiceActivity</b>, you determine whether the batch work is done synchronously or asynchronously. The batch work itself is implemented through the <a href="https://msdn.microsoft.com/97532e29-3d1a-4a7c-8103-dd7ae2866a70">IServiceCall</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/5ef67411-334b-476e-b9b7-3677b24ab7df">COM+ Services Without Components</a>



<a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a>



<a href="https://msdn.microsoft.com/84640b3b-1f43-4bec-abf6-c295cfb3da8b">CoEnterServiceDomain</a>



<a href="https://msdn.microsoft.com/b67b3cf6-4462-4578-b61b-c5c61d809822">CoLeaveServiceDomain</a>



<a href="https://msdn.microsoft.com/005bf0ec-f5a7-41a3-85b3-07f79f26af27">IServiceActivity</a>



<a href="https://msdn.microsoft.com/97532e29-3d1a-4a7c-8103-dd7ae2866a70">IServiceCall</a>
 

 

