---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WS_CERTIFICATE_VALIDATION_CALLBACK callback function


## -description


The <i>WS_CERTIFICATE_VALIDATION_CALLBACK</i> callback is invoked to validate a certificate when a connection to an HTTP server has been established and headers sent.


## -parameters




### -param certContext [in]

A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that is associated with the connection. Applications must free this structure using <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>.


### -param *state [in, optional]

A pointer to application specific state information. This parameter corresponds to the <b>state</b> member of the <a href="https://msdn.microsoft.com/1D33A816-2580-4295-994D-6C6DFFBA7A0B">WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT</a> structure.


## -returns



This callback function can return one of these values.

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

The certificate validated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks



If <i>WS_CERTIFICATE_VALIDATION_CALLBACK</i> returns any value other than <b>S_OK</b>, the channel will be aborted. The service proxy will also be aborted if this property was passed to <a href="https://msdn.microsoft.com/9215684b-979e-48ad-b4ee-2ae1db1e3034">WsCreateServiceProxy</a>.

The callback implementation must avoid long computation times or long blocking calls so that it returns to the caller quickly.




## -see-also




<a href="https://msdn.microsoft.com/1D33A816-2580-4295-994D-6C6DFFBA7A0B">WS_CERTIFICATE_VALIDATION_CALLBACK_CONTEXT</a>
 

 

