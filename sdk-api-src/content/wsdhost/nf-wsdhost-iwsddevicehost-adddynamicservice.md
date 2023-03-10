---
UID: NF:wsdhost.IWSDDeviceHost.AddDynamicService
title: IWSDDeviceHost::AddDynamicService (wsdhost.h)
description: Registers a service object for incoming requests, but does not add the service to the device host metadata. This is used for transient (dynamic) services.
helpviewer_keywords: ["AddDynamicService","AddDynamicService method","AddDynamicService method","IWSDDeviceHost interface","IWSDDeviceHost interface","AddDynamicService method","IWSDDeviceHost.AddDynamicService","IWSDDeviceHost::AddDynamicService","ncd.iwsddevicehost_adddynamicservice_method","wsdhost/IWSDDeviceHost::AddDynamicService"]
old-location: ncd\iwsddevicehost_adddynamicservice_method.htm
tech.root: ncd
ms.assetid: 0ef7760d-39eb-48fe-a7e9-043c2b9ba5a4
ms.date: 12/05/2018
ms.keywords: AddDynamicService, AddDynamicService method, AddDynamicService method,IWSDDeviceHost interface, IWSDDeviceHost interface,AddDynamicService method, IWSDDeviceHost.AddDynamicService, IWSDDeviceHost::AddDynamicService, ncd.iwsddevicehost_adddynamicservice_method, wsdhost/IWSDDeviceHost::AddDynamicService
req.header: wsdhost.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdHost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDDeviceHost::AddDynamicService
 - wsdhost/IWSDDeviceHost::AddDynamicService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDDeviceHost.AddDynamicService
---

# IWSDDeviceHost::AddDynamicService


## -description

Registers a service object for incoming requests, but does not add the service to the device host metadata. This is used for transient (dynamic) services.

## -parameters

### -param pszServiceId [in]

The ID for the dynamic service. The service ID must be distinct from all the service IDs in the service host metadata and from any other registered dynamic service. The <i>pszServiceId</i> must be a URI.

### -param pszEndpointAddress [in, optional]

An optional URI to use as the endpoint address for this service. If none is specified, the device host will assume the service should be available on all local transport addresses.

### -param pPortType [in, optional]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_port_type">WSD_PORT_TYPE</a> structure that specifies the port type. 
May be <b>NULL</b>. Specify only one of <i>pPortType</i> and <i>pPortName</i>.

### -param pPortName [in, optional]

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_name">WSDXML_NAME</a> structure that specifies the type of the service, with associating the service with a specified port. Specify only one of <i>pPortType</i> and <i>pPortName</i>.

### -param pAny [in, optional]

Optional reference to an extensible section to be included in the dynamic service metadata.

### -param pService [in, optional]

 Optional reference to a host service object to register.

## -returns

Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pszServiceId</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The length in characters of <i>pszServiceId</i> or <i>pszEndpointAddress</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or both <i>pPortType</i> and <i>pPortName</i> are specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed. It may have failed because the host has not been initialized, or the service specified by <i>pszServiceId</i> could not be found. Call <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-init">Init</a> to initialize a device host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>

## -remarks

When this method is called, the device adds a reference to the service object and calls its methods in response to request messages addressed to the service. Call the <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-removedynamicservice">RemoveDynamicService</a> method on the device host to release its reference to the service and stop calling methods on the service.

## -see-also

<a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a>