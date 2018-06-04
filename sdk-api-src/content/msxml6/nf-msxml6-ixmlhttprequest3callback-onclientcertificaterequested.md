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

# IXMLHTTPRequest3Callback::OnClientCertificateRequested


## -description


Occurs when a client receives a request for a client certificate during SSL negotiation with the server.


## -parameters




### -param pXHR [in]

The initial HTTP request.


### -param cIssuerList [in]

The number of strings in the <i>rgpwszIssuerList</i> parameter.


### -param rgpwszIssuerList [in]

An array of strings that represent the issuer list.


## -returns



Returns <b>S_OK</b> on success.




## -remarks



<div class="alert"><b>Note</b>  This callback method must not throw exceptions.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a>



<a href="https://msdn.microsoft.com/f745669a-a594-457d-ae6b-952a55576bae">IXMLHTTPRequest3Callback</a>



<a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a>
 

 

