---
UID: NF:wsdbase.IWSDSSLClientCertificate.GetMappedAccessToken
title: IWSDSSLClientCertificate::GetMappedAccessToken
author: windows-sdk-content
description: Gets the mapped access token.
old-location: ncd\iwsdsslclientcertificate_getmappedaccesstoken.htm
old-project: WsdApi
ms.assetid: 79dbd838-cffd-4571-8227-e508673c1b02
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetMappedAccessToken, GetMappedAccessToken method, GetMappedAccessToken method,IWSDSSLClientCertificate interface, IWSDSSLClientCertificate interface,GetMappedAccessToken method, IWSDSSLClientCertificate.GetMappedAccessToken, IWSDSSLClientCertificate::GetMappedAccessToken, ncd.iwsdsslclientcertificate_getmappedaccesstoken, wsdbase/IWSDSSLClientCertificate::GetMappedAccessToken
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDSSLClientCertificate.GetMappedAccessToken
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

