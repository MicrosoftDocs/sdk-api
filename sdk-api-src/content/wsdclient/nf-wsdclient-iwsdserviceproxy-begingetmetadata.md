---
UID: NF:wsdclient.IWSDServiceProxy.BeginGetMetadata
title: IWSDServiceProxy::BeginGetMetadata
author: windows-driver-content
description: Initiates an asynchronous metadata exchange request with the remote service.
old-location: ncd\iwsdserviceproxy_begingetmetadata.htm
old-project: WsdApi
ms.assetid: bcc0bcaf-76fb-4dca-b946-2826809a53a1
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: BeginGetMetadata, BeginGetMetadata method, BeginGetMetadata method,IWSDServiceProxy interface, IWSDServiceProxy interface,BeginGetMetadata method, IWSDServiceProxy.BeginGetMetadata, IWSDServiceProxy::BeginGetMetadata, ncd.iwsdserviceproxy_begingetmetadata, wsdclient/IWSDServiceProxy::BeginGetMetadata
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
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDServiceProxy.BeginGetMetadata
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDServiceProxy::BeginGetMetadata


## -description


Initiates an asynchronous metadata exchange request with the remote service.


## -parameters




### -param ppResult [out]

An <a href="https://msdn.microsoft.com/49c5ad02-f24b-4ef9-b943-483728c0bbcd">IWSDAsyncResult</a> interface that you use to poll for the result, register a callback object, or configure an event to be signaled when the response is received.


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
<i>ppResult</i> is <b>NULL</b>.

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
 




## -remarks



Call <a href="https://msdn.microsoft.com/6024770a-e4cb-4db1-9767-51b559fd8244">IWSDServiceProxy::EndGetMetadata</a> to complete the asynchronous operation and to retrieve the metadata.




## -see-also




<a href="https://msdn.microsoft.com/8753bcc8-f0c3-4dd0-8ebe-f6c15a271c70">IWSDServiceProxy</a>
 

 

