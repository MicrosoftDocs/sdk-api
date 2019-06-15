---
UID: NF:wsdclient.IWSDServiceProxy.GetEndpointProxy
title: IWSDServiceProxy::GetEndpointProxy (wsdclient.h)
author: windows-sdk-content
description: Gets the endpoint proxy for the device.
old-location: ncd\iwsdserviceproxy_getendpointproxy.htm
tech.root: WsdApi
ms.assetid: 9c236f31-e3ba-4678-a4fe-1e078c9f9af3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetEndpointProxy, GetEndpointProxy method, GetEndpointProxy method,IWSDServiceProxy interface, IWSDServiceProxy interface,GetEndpointProxy method, IWSDServiceProxy.GetEndpointProxy, IWSDServiceProxy::GetEndpointProxy, ncd.iwsdserviceproxy_getendpointproxy, wsdclient/IWSDServiceProxy::GetEndpointProxy
ms.topic: method
f1_keywords: ["wsdclient/IWSDServiceProxy.GetEndpointProxy"]
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
 - IWSDServiceProxy.GetEndpointProxy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDServiceProxy::GetEndpointProxy


## -description


Gets the endpoint proxy for the device.


## -parameters




### -param ppProxy [out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nn-wsdclient-iwsdendpointproxy">IWSDEndpointProxy</a> interface.


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
<i>ppProxy</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The endpoint proxy is provided if a fault was received for a prior request. The client can then call <a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nf-wsdclient-iwsdendpointproxy-getfaultinfo">IWSDEndpointProxy::GetFaultInfo</a> to determine the nature of the error.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsdclient/nn-wsdclient-iwsdserviceproxy">IWSDServiceProxy</a>
 

 

