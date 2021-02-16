---
UID: NF:wsdbase.IWSDSSLClientCertificate.GetMappedAccessToken
title: IWSDSSLClientCertificate::GetMappedAccessToken (wsdbase.h)
description: Gets the mapped access token.
helpviewer_keywords: ["GetMappedAccessToken","GetMappedAccessToken method","GetMappedAccessToken method","IWSDSSLClientCertificate interface","IWSDSSLClientCertificate interface","GetMappedAccessToken method","IWSDSSLClientCertificate.GetMappedAccessToken","IWSDSSLClientCertificate::GetMappedAccessToken","ncd.iwsdsslclientcertificate_getmappedaccesstoken","wsdbase/IWSDSSLClientCertificate::GetMappedAccessToken"]
old-location: ncd\iwsdsslclientcertificate_getmappedaccesstoken.htm
tech.root: ncd
ms.assetid: 79dbd838-cffd-4571-8227-e508673c1b02
ms.date: 12/05/2018
ms.keywords: GetMappedAccessToken, GetMappedAccessToken method, GetMappedAccessToken method,IWSDSSLClientCertificate interface, IWSDSSLClientCertificate interface,GetMappedAccessToken method, IWSDSSLClientCertificate.GetMappedAccessToken, IWSDSSLClientCertificate::GetMappedAccessToken, ncd.iwsdsslclientcertificate_getmappedaccesstoken, wsdbase/IWSDSSLClientCertificate::GetMappedAccessToken
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDSSLClientCertificate::GetMappedAccessToken
 - wsdbase/IWSDSSLClientCertificate::GetMappedAccessToken
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
 - IWSDSSLClientCertificate.GetMappedAccessToken
---

# IWSDSSLClientCertificate::GetMappedAccessToken


## -description

Gets the mapped access token.

## -parameters

### -param phToken [in, out]

A handle for the mapped access token. Upon completion, the caller must free the handle by  calling <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.

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

If the client certificate was successfully mapped to an operating system user account, then a valid access token for this user will be returned through <i>phToken</i>. This token can be used to impersonate the user. Internally, HTTP.sys will do the client certificate to user account mapping and return this information through the <a href="/windows/desktop/api/http/ns-http-http_ssl_client_cert_info">HTTP_SSL_CLIENT_CERT_INFO</a> structure.

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdsslclientcertificate">IWSDSSLClientCertificate</a>