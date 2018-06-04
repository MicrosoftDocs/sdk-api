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

# IWSDSSLClientCertificate::GetMappedAccessToken


## -description


Gets the mapped access token.


## -parameters




### -param phToken [in, out]

A handle for the mapped access token. Upon completion, the caller must free the handle by  calling <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The  token associated with the specified handle is not available.

</td>
</tr>
</table>
 




## -remarks



If the client certificate was successfully mapped to an operating system user account, then a valid access token for this user will be returned through <i>phToken</i>. This token can be used to impersonate the user. Internally, HTTP.sys will do the client certificate to user account mapping and return this information through the <a href="https://msdn.microsoft.com/bfe6a9a9-6117-4403-a83f-e9448615500b">HTTP_SSL_CLIENT_CERT_INFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/d1b5eb99-7bbb-4881-8251-4362368dff88">IWSDSSLClientCertificate</a>
 

 

