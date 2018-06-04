---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFunctionDiscoveryProvider::InstanceQueryService


## -description


<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a provider-specific COM object for the function instance. Provider writers can implement this method to offer additional functionality through the COM object.


## -parameters




### -param pIFunctionInstance [in]

A pointer to the <a href="https://msdn.microsoft.com/cc421719-73a6-4d4d-9bf8-171e46c4e275">IFunctionInstance</a> interface.


### -param iProviderInstanceContext [in]

The context associated with the specific function instance.


### -param guidService [in]

The unique identifier of the service (a SID). This is the service ID defined by the provider writer. For an example, see FunctionDiscoveryServiceIDs.h.


### -param riid [in]

The unique identifier of the interface the caller wishes to receive for the service.


### -param ppIUnknown [out]

A pointer that receives the interface pointer of the service.  The caller is responsible for calling <b>Release</b> through this interface pointer when the service is no longer needed.


## -returns



Possible return values include, but are not limited to, the following.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The provider does implement the service identified by <i>guidService</i> but does not implement the interface identified by <i>rrid</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The provider does not implement the <a href="https://msdn.microsoft.com/04d29632-81b3-47d6-8630-a65677d78b6f">IFunctionInstance::QueryService</a> method, or the service identifier specified by <i>guidService</i> does not match the provider's service identifier.

</td>
</tr>
</table>
 




## -remarks



<b>InstanceQueryService</b> creates or accesses the implementation the service identified with <i>guidService</i>, returning the address of the interface specified by <i>riid</i> in the <i>ppv</i> argument.  Providers can implement the service and this method provides a mechanism for the provider to supply this implementation rather then requiring the creation of a new object to implement the service.

The provider should return <b>E_NOINTERFACE</b> if the <i>guidService</i> does not belong to this provider, or the <i>riid</i> interface  is not supported.  The provider should return <b>E_NOTIMPL</b> if it simply does not implement this method or does not implement the requested SID.

Any provider that supports embedded services or devices must implement the SID_PNPXServiceCollection service.  If the SID_PNPXServiceCollection service is supported, the client can call <a href="https://msdn.microsoft.com/04d29632-81b3-47d6-8630-a65677d78b6f">IFunctionInstance::QueryService</a> to access the information and metadata associated with the embedded services or devices. For example, the PnP-X providers (that is, the <a href="https://msdn.microsoft.com/41d65b08-7601-430e-9702-6a6fd9854027">SSDP provider</a> and the WSD provider) implement support for the SID_PNPXServiceCollection service. Not all providers implement SID_PNPXServiceCollection service support.




## -see-also




<a href="https://msdn.microsoft.com/e0019d0d-1495-4a0e-a7d9-7772046a4a26">IFunctionDiscoveryProvider</a>
 

 

