---
UID: NF:wsdclient.IWSDDeviceProxy.GetServiceProxyById
title: IWSDDeviceProxy::GetServiceProxyById (wsdclient.h)
description: Retrieves a generic IWSDServiceProxy service proxy by service ID.
helpviewer_keywords: ["GetServiceProxyById","GetServiceProxyById method","GetServiceProxyById method","IWSDDeviceProxy interface","IWSDDeviceProxy interface","GetServiceProxyById method","IWSDDeviceProxy.GetServiceProxyById","IWSDDeviceProxy::GetServiceProxyById","ncd.iwsddeviceproxy_getserviceproxybyid_method","wsdclient/IWSDDeviceProxy::GetServiceProxyById"]
old-location: ncd\iwsddeviceproxy_getserviceproxybyid_method.htm
tech.root: ncd
ms.assetid: c1c07b78-16f6-4595-8de3-0c6591096496
ms.date: 12/05/2018
ms.keywords: GetServiceProxyById, GetServiceProxyById method, GetServiceProxyById method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,GetServiceProxyById method, IWSDDeviceProxy.GetServiceProxyById, IWSDDeviceProxy::GetServiceProxyById, ncd.iwsddeviceproxy_getserviceproxybyid_method, wsdclient/IWSDDeviceProxy::GetServiceProxyById
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
 - IWSDDeviceProxy::GetServiceProxyById
 - wsdclient/IWSDDeviceProxy::GetServiceProxyById
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
 - IWSDDeviceProxy.GetServiceProxyById
---

# IWSDDeviceProxy::GetServiceProxyById


## -description

Retrieves a generic <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a> service proxy by service ID. Service IDs can be obtained by examining the service host metadata.

## -parameters

### -param pszServiceId [in]

The service ID.

### -param ppServiceProxy [out]

Pointer to an <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a> object for the specified service proxy.

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
<i>ppServiceProxy</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The length in characters of <i>pszServiceId</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or there is no metadata associated with the service specified by  <i>pszServiceId</i>.

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

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a>