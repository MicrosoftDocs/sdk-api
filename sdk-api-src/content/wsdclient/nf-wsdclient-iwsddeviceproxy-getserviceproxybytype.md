---
UID: NF:wsdclient.IWSDDeviceProxy.GetServiceProxyByType
title: IWSDDeviceProxy::GetServiceProxyByType (wsdclient.h)
description: Retrieves a generic IWSDServiceProxy proxy for a service exposed by the device by port type name.
helpviewer_keywords: ["GetServiceProxyByType","GetServiceProxyByType method","GetServiceProxyByType method","IWSDDeviceProxy interface","IWSDDeviceProxy interface","GetServiceProxyByType method","IWSDDeviceProxy.GetServiceProxyByType","IWSDDeviceProxy::GetServiceProxyByType","ncd.iwsddeviceproxy_getserviceproxybytype_method","wsdclient/IWSDDeviceProxy::GetServiceProxyByType"]
old-location: ncd\iwsddeviceproxy_getserviceproxybytype_method.htm
tech.root: ncd
ms.assetid: 20df9a62-b983-40ed-a4bc-07131b80de6e
ms.date: 12/05/2018
ms.keywords: GetServiceProxyByType, GetServiceProxyByType method, GetServiceProxyByType method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,GetServiceProxyByType method, IWSDDeviceProxy.GetServiceProxyByType, IWSDDeviceProxy::GetServiceProxyByType, ncd.iwsddeviceproxy_getserviceproxybytype_method, wsdclient/IWSDDeviceProxy::GetServiceProxyByType
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
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
 - IWSDDeviceProxy::GetServiceProxyByType
 - wsdclient/IWSDDeviceProxy::GetServiceProxyByType
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
 - IWSDDeviceProxy.GetServiceProxyByType
---

# IWSDDeviceProxy::GetServiceProxyByType


## -description

Retrieves a generic <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a> proxy for a service exposed by the device by port type name.

## -parameters

### -param pType [in]

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_name">WSDXML_NAME</a> structure that specifies the port type name.

### -param ppServiceProxy [out]

Pointer to the <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a> object associated with the specified service.

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
<i>pType</i> or <i>ppServiceProxy</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
There is no metadata associated with the service specified by  <i>pType</i>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
There is no endpoint associated with the service proxy.

</td>
</tr>
</table>

## -remarks

If the device hosts more than one service of the specified type, a proxy for any one of the services may be returned. In such a case, callers should not depend on any particular service proxy being returned.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a>