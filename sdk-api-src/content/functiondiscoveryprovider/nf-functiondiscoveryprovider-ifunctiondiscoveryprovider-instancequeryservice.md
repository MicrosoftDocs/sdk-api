---
UID: NF:functiondiscoveryprovider.IFunctionDiscoveryProvider.InstanceQueryService
title: IFunctionDiscoveryProvider::InstanceQueryService (functiondiscoveryprovider.h)
description: Creates a provider-specific COM object for the function instance.
helpviewer_keywords: ["IFunctionDiscoveryProvider interface","InstanceQueryService method","IFunctionDiscoveryProvider.InstanceQueryService","IFunctionDiscoveryProvider::InstanceQueryService","InstanceQueryService","InstanceQueryService method","InstanceQueryService method","IFunctionDiscoveryProvider interface","functiondiscoveryprovider/IFunctionDiscoveryProvider::InstanceQueryService","ncd.ifunctiondiscoveryprovider_instancequeryservice_method"]
old-location: ncd\ifunctiondiscoveryprovider_instancequeryservice_method.htm
tech.root: ncd
ms.assetid: 8fb955dd-f396-4473-a1c1-b0d83e2b4b07
ms.date: 12/05/2018
ms.keywords: IFunctionDiscoveryProvider interface,InstanceQueryService method, IFunctionDiscoveryProvider.InstanceQueryService, IFunctionDiscoveryProvider::InstanceQueryService, InstanceQueryService, InstanceQueryService method, InstanceQueryService method,IFunctionDiscoveryProvider interface, functiondiscoveryprovider/IFunctionDiscoveryProvider::InstanceQueryService, ncd.ifunctiondiscoveryprovider_instancequeryservice_method
req.header: functiondiscoveryprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryProvider.idl
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
 - IFunctionDiscoveryProvider::InstanceQueryService
 - functiondiscoveryprovider/IFunctionDiscoveryProvider::InstanceQueryService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunctionDiscoveryProvider.h
api_name:
 - IFunctionDiscoveryProvider.InstanceQueryService
---

# IFunctionDiscoveryProvider::InstanceQueryService


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a provider-specific COM object for the function instance. Provider writers can implement this method to offer additional functionality through the COM object.

## -parameters

### -param pIFunctionInstance [in]

A pointer to the <a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstance">IFunctionInstance</a> interface.

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
The provider does not implement the <a href="/previous-versions/windows/desktop/legacy/aa364381(v=vs.85)">IFunctionInstance::QueryService</a> method, or the service identifier specified by <i>guidService</i> does not match the provider's service identifier.

</td>
</tr>
</table>

## -remarks

<b>InstanceQueryService</b> creates or accesses the implementation the service identified with <i>guidService</i>, returning the address of the interface specified by <i>riid</i> in the <i>ppv</i> argument.  Providers can implement the service and this method provides a mechanism for the provider to supply this implementation rather then requiring the creation of a new object to implement the service.

The provider should return <b>E_NOINTERFACE</b> if the <i>guidService</i> does not belong to this provider, or the <i>riid</i> interface  is not supported.  The provider should return <b>E_NOTIMPL</b> if it simply does not implement this method or does not implement the requested SID.

Any provider that supports embedded services or devices must implement the SID_PNPXServiceCollection service.  If the SID_PNPXServiceCollection service is supported, the client can call <a href="/previous-versions/windows/desktop/legacy/aa364381(v=vs.85)">IFunctionInstance::QueryService</a> to access the information and metadata associated with the embedded services or devices. For example, the PnP-X providers (that is, the <a href="/previous-versions/windows/desktop/fundisc/ssdp-provider">SSDP provider</a> and the WSD provider) implement support for the SID_PNPXServiceCollection service. Not all providers implement SID_PNPXServiceCollection service support.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryprovider/nn-functiondiscoveryprovider-ifunctiondiscoveryprovider">IFunctionDiscoveryProvider</a>