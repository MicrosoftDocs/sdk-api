---
UID: NF:wsdhost.IWSDServiceMessaging.FaultRequest
title: IWSDServiceMessaging::FaultRequest (wsdhost.h)
description: Sends a fault matching a given request context.
helpviewer_keywords: ["FaultRequest","FaultRequest method","FaultRequest method","IWSDServiceMessaging interface","IWSDServiceMessaging interface","FaultRequest method","IWSDServiceMessaging.FaultRequest","IWSDServiceMessaging::FaultRequest","ncd.iwsdservicemessaging_faultrequest","wsdhost/IWSDServiceMessaging::FaultRequest"]
old-location: ncd\iwsdservicemessaging_faultrequest.htm
tech.root: ncd
ms.assetid: 478cf63e-7cfe-4f6f-af7f-d288588d9c8d
ms.date: 12/05/2018
ms.keywords: FaultRequest, FaultRequest method, FaultRequest method,IWSDServiceMessaging interface, IWSDServiceMessaging interface,FaultRequest method, IWSDServiceMessaging.FaultRequest, IWSDServiceMessaging::FaultRequest, ncd.iwsdservicemessaging_faultrequest, wsdhost/IWSDServiceMessaging::FaultRequest
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDServiceMessaging::FaultRequest
 - wsdhost/IWSDServiceMessaging::FaultRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDServiceMessaging.FaultRequest
---

# IWSDServiceMessaging::FaultRequest


## -description

Sends a fault matching a given request context.  This method should be called only from <a href="/windows/desktop/WsdApi/web-services-for-devices-code-generator">generated code</a>.

## -parameters

### -param pRequestHeader [in]

Pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_header">WSD_SOAP_HEADER</a> structure that contains the SOAP header of the original request that caused the fault.

### -param pMessageParameters [in]

Pointer to an <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a> object that contains the message parameters for the original request that caused the fault.

### -param pFault [in, optional]

Pointer to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_soap_fault">WSD_SOAP_FAULT</a> structure that describes the fault to serialize and send. If this parameter is omitted, a fault of type <b>wsa:EndpointUnavailable</b> will be sent.

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

<a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsdservicemessaging">IWSDServiceMessaging</a>