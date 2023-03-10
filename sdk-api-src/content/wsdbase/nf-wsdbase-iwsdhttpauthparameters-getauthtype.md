---
UID: NF:wsdbase.IWSDHttpAuthParameters.GetAuthType
title: IWSDHttpAuthParameters::GetAuthType (wsdbase.h)
description: GetAuthType method retrieves the HTTP authentication scheme used during the authentication of the client.
helpviewer_keywords: ["GetAuthType","GetAuthType method","GetAuthType method","IWSDHttpAuthParameters interface","IWSDHttpAuthParameters interface","GetAuthType method","IWSDHttpAuthParameters.GetAuthType","IWSDHttpAuthParameters::GetAuthType","WSD_SECURITY_HTTP_AUTH_SCHEME_NEGOTIATE","WSD_SECURITY_HTTP_AUTH_SCHEME_NTLM","ncd.iwsdhttpauthparameters_getauthtype","wsdbase/IWSDHttpAuthParameters::GetAuthType"]
old-location: ncd\iwsdhttpauthparameters_getauthtype.htm
tech.root: ncd
ms.assetid: F5D218DD-474B-4562-8877-D159394AF365
ms.date: 12/05/2018
ms.keywords: GetAuthType, GetAuthType method, GetAuthType method,IWSDHttpAuthParameters interface, IWSDHttpAuthParameters interface,GetAuthType method, IWSDHttpAuthParameters.GetAuthType, IWSDHttpAuthParameters::GetAuthType, WSD_SECURITY_HTTP_AUTH_SCHEME_NEGOTIATE, WSD_SECURITY_HTTP_AUTH_SCHEME_NTLM, ncd.iwsdhttpauthparameters_getauthtype, wsdbase/IWSDHttpAuthParameters::GetAuthType
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDHttpAuthParameters::GetAuthType
 - wsdbase/IWSDHttpAuthParameters::GetAuthType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdbase.h
api_name:
 - IWSDHttpAuthParameters.GetAuthType
---

# IWSDHttpAuthParameters::GetAuthType


## -description

The <b>GetAuthType</b> method retrieves the HTTP authentication scheme used during the authentication of the client.

## -parameters

### -param pAuthType

Pointer to an <a href="/windows/desktop/api/http/ne-http-http_request_auth_type">HTTP_REQUEST_AUTH_TYPE</a>  value that indicates the HTTP authentication scheme used during authentication. Possible values include:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WSD_SECURITY_HTTP_AUTH_SCHEME_NEGOTIATE_"></a><a id="wsd_security_http_auth_scheme_negotiate_"></a><dl>
<dt><b>WSD_SECURITY_HTTP_AUTH_SCHEME_NEGOTIATE </b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Negotiate authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="WSD_SECURITY_HTTP_AUTH_SCHEME_NTLM"></a><a id="wsd_security_http_auth_scheme_ntlm"></a><dl>
<dt><b>WSD_SECURITY_HTTP_AUTH_SCHEME_NTLM</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
NTLM authentication.

</td>
</tr>
</table>

## -returns

This method returns S_OK on success.

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpauthparameters">IWSDHttpAuthParameters</a>