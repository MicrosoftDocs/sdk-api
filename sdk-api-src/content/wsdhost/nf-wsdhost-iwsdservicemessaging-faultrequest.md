---
UID: NF:wsdhost.IWSDServiceMessaging.FaultRequest
title: IWSDServiceMessaging::FaultRequest
author: windows-sdk-content
description: Sends a fault matching a given request context.
old-location: ncd\iwsdservicemessaging_faultrequest.htm
tech.root: WsdApi
ms.assetid: 478cf63e-7cfe-4f6f-af7f-d288588d9c8d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FaultRequest, FaultRequest method, FaultRequest method,IWSDServiceMessaging interface, IWSDServiceMessaging interface,FaultRequest method, IWSDServiceMessaging.FaultRequest, IWSDServiceMessaging::FaultRequest, ncd.iwsdservicemessaging_faultrequest, wsdhost/IWSDServiceMessaging::FaultRequest
ms.topic: method
req.header: wsdhost.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdhost.idl
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
 - wsdapi.dll
api_name:
 - IWSDServiceMessaging.FaultRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDServiceMessaging::FaultRequest


## -description


Sends a fault matching a given request context.  This method should be called only from <a href="https://msdn.microsoft.com/76dffca8-bb84-4384-a9e8-120a4cf2acac">generated code</a>.


## -parameters




### -param pRequestHeader [in]

Pointer to a <a href="https://msdn.microsoft.com/6a0f0fd3-486e-45b3-bac6-e241bce8e2dc">WSD_SOAP_HEADER</a> structure that contains the SOAP header of the original request that caused the fault.


### -param pMessageParameters [in]

Pointer to an <a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a> object that contains the message parameters for the original request that caused the fault.


### -param pFault [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/ed5e2575-203a-41a2-b656-50cb82aae088">WSD_SOAP_FAULT</a> structure that describes the fault to serialize and send. If this parameter is omitted, a fault of type <b>wsa:EndpointUnavailable</b> will be sent.


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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pRequestHeader</i> or <i>pMessageParameters</i> is <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The method could not be completed.

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
The method failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/06584474-1c55-43db-9c7a-fefea8d16eed">IWSDServiceMessaging</a>
 

 

