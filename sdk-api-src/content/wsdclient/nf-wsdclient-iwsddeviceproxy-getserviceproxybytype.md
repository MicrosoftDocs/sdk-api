---
UID: NF:wsdclient.IWSDDeviceProxy.GetServiceProxyByType
title: IWSDDeviceProxy::GetServiceProxyByType
author: windows-sdk-content
description: Retrieves a generic IWSDServiceProxy proxy for a service exposed by the device by port type name.
old-location: ncd\iwsddeviceproxy_getserviceproxybytype_method.htm
tech.root: WsdApi
ms.assetid: 20df9a62-b983-40ed-a4bc-07131b80de6e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetServiceProxyByType, GetServiceProxyByType method, GetServiceProxyByType method,IWSDDeviceProxy interface, IWSDDeviceProxy interface,GetServiceProxyByType method, IWSDDeviceProxy.GetServiceProxyByType, IWSDDeviceProxy::GetServiceProxyByType, ncd.iwsddeviceproxy_getserviceproxybytype_method, wsdclient/IWSDDeviceProxy::GetServiceProxyByType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDDeviceProxy.GetServiceProxyByType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wsdclient.h
: 
- IWSDDeviceProxy.GetServiceProxyByType
: 
---

# IWSDDeviceProxy::GetServiceProxyByType


## -description


Retrieves a generic <a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a> proxy for a service exposed by the device by port type name.


## -parameters




### -param pType [in]

Reference to a <a href="https://msdn.microsoft.com/9dce71d2-700c-4f86-9308-dee6a69010bb">WSDXML_NAME</a> structure that specifies the port type name. 



### -param ppServiceProxy [out]

Pointer to the <a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a> object associated with the specified service. 



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




<a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a>
 

 

