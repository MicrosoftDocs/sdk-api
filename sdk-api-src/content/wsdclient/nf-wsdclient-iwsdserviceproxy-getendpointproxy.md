---
UID: NF:wsdclient.IWSDServiceProxy.GetEndpointProxy
title: IWSDServiceProxy::GetEndpointProxy
author: windows-sdk-content
description: Gets the endpoint proxy for the device.
old-location: ncd\iwsdserviceproxy_getendpointproxy.htm
old-project: wsdapi
ms.assetid: 9c236f31-e3ba-4678-a4fe-1e078c9f9af3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetEndpointProxy, GetEndpointProxy method, GetEndpointProxy method,IWSDServiceProxy interface, IWSDServiceProxy interface,GetEndpointProxy method, IWSDServiceProxy.GetEndpointProxy, IWSDServiceProxy::GetEndpointProxy, ncd.iwsdserviceproxy_getendpointproxy, wsdclient/IWSDServiceProxy::GetEndpointProxy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.redist: 
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
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDServiceProxy::GetEndpointProxy


## -description


Gets the endpoint proxy for the device.


## -parameters




### -param ppProxy [out]

Pointer to an <a href="https://msdn.microsoft.com/58ca085f-8939-413c-8fd3-4d867b1cf490">IWSDEndpointProxy</a> interface.


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



The endpoint proxy is provided if a fault was received for a prior request. The client can then call <a href="https://msdn.microsoft.com/45ed30fd-7e4f-44f5-bb90-5686746e39be">IWSDEndpointProxy::GetFaultInfo</a> to determine the nature of the error.




## -see-also




<a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a>
 

 

