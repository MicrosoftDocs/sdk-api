---
UID: NE:wsdbase.__MIDL___MIDL_itf_wsdbase_0000_0000_0001
title: "__MIDL___MIDL_itf_wsdbase_0000_0000_0001"
author: windows-driver-content
description: Specifies the kind of data stored in a WSD_CONFIG_PARAM structure.
old-location: ncd\wsd_config_param_type.htm
old-project: WsdApi
ms.assetid: 46189d61-79d0-4ec9-82eb-ac1331201490
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: WSD_CONFIG_DEVICE_ADDRESSES, WSD_CONFIG_HOSTING_ADDRESSES, WSD_CONFIG_MAX_INBOUND_MESSAGE_SIZE, WSD_CONFIG_MAX_OUTBOUND_MESSAGE_SIZE, WSD_CONFIG_PARAM_TYPE, WSD_CONFIG_PARAM_TYPE enumeration, WSD_SECURITY_COMPACTSIG_SIGNING_CERT, WSD_SECURITY_COMPACTSIG_VALIDATION, WSD_SECURITY_REQUIRE_CLIENT_CERT_OR_HTTP_CLIENT_AUTH, WSD_SECURITY_REQUIRE_HTTP_CLIENT_AUTH, WSD_SECURITY_SSL_CERT_FOR_CLIENT_AUTH, WSD_SECURITY_SSL_CLIENT_CERT_VALIDATION, WSD_SECURITY_SSL_NEGOTIATE_CLIENT_CERT, WSD_SECURITY_SSL_SERVER_CERT_VALIDATION, WSD_SECURITY_USE_HTTP_CLIENT_AUTH, __MIDL___MIDL_itf_wsdbase_0000_0000_0001, ncd.wsd_config_param_type, wsdbase/WSD_CONFIG_DEVICE_ADDRESSES, wsdbase/WSD_CONFIG_HOSTING_ADDRESSES, wsdbase/WSD_CONFIG_MAX_INBOUND_MESSAGE_SIZE, wsdbase/WSD_CONFIG_MAX_OUTBOUND_MESSAGE_SIZE, wsdbase/WSD_CONFIG_PARAM_TYPE, wsdbase/WSD_SECURITY_COMPACTSIG_SIGNING_CERT, wsdbase/WSD_SECURITY_COMPACTSIG_VALIDATION, wsdbase/WSD_SECURITY_REQUIRE_CLIENT_CERT_OR_HTTP_CLIENT_AUTH, wsdbase/WSD_SECURITY_REQUIRE_HTTP_CLIENT_AUTH, wsdbase/WSD_SECURITY_SSL_CERT_FOR_CLIENT_AUTH, wsdbase/WSD_SECURITY_SSL_CLIENT_CERT_VALIDATION, wsdbase/WSD_SECURITY_SSL_NEGOTIATE_CLIENT_CERT, wsdbase/WSD_SECURITY_SSL_SERVER_CERT_VALIDATION, wsdbase/WSD_SECURITY_USE_HTTP_CLIENT_AUTH
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: wsdbase.h
req.include-header: Windows.h
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
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wsdbase.h
api_name:
-	WSD_CONFIG_PARAM_TYPE
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# __MIDL___MIDL_itf_wsdbase_0000_0000_0001 enumeration


## -description


Specifies the kind of data stored in a 
    <a href="https://msdn.microsoft.com/58dc3e11-586e-4185-b1d0-4249b4bfb252">WSD_CONFIG_PARAM</a> structure.


## -enum-fields




### -field WSD_CONFIG_MAX_INBOUND_MESSAGE_SIZE

The <i>pConfigData</i> member is a pointer to a <b>DWORD</b> that specifies the maximum size,  in octets, of an inbound message.

The <i>dwConfigDataSize</i> member is 4.


### -field WSD_CONFIG_MAX_OUTBOUND_MESSAGE_SIZE

The <i>pConfigData</i> member is a pointer to a <b>DWORD</b> that specifies the maximum size, in octets, of an outbound message.

The <i>dwConfigDataSize</i> member is 4.


### -field WSD_SECURITY_SSL_CERT_FOR_CLIENT_AUTH

Used to pass in the client certificate that WSDAPI will use for client authentication in an SSL connection.

The <i>pConfigData</i> member is a pointer to a  <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that represents the client certificate.  The caller needs to have read access to the private key of the certificate.

The <i>dwConfigDataSize</i> member is the size of the <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure.


### -field WSD_SECURITY_SSL_SERVER_CERT_VALIDATION

Used to pass in the SSL server certificate validation information into WSDAPI.  When establishing the SSL connection, WSDAPI will accept only a server certificate that matches the criteria specified by the <a href="https://msdn.microsoft.com/1bc157c2-f3c2-4b67-a6ae-251ba1cb0379">WSD_SECURITY_CERT_VALIDATION</a> structure.

The <i>pConfigData</i> member is a pointer to a <a href="https://msdn.microsoft.com/1bc157c2-f3c2-4b67-a6ae-251ba1cb0379">WSD_SECURITY_CERT_VALIDATION</a> structure.

The <i>dwConfigDataSize</i> member is the size of the <a href="https://msdn.microsoft.com/1bc157c2-f3c2-4b67-a6ae-251ba1cb0379">WSD_SECURITY_CERT_VALIDATION</a> structure.


### -field WSD_SECURITY_SSL_CLIENT_CERT_VALIDATION

Used to pass in the SSL client certificate validation information into WSDAPI.  On incoming SSL connections, if a client certificate is available, WSDAPI will reject the connection if the client certificate doesn't match the validation criteria specified by the <a href="https://msdn.microsoft.com/1bc157c2-f3c2-4b67-a6ae-251ba1cb0379">WSD_SECURITY_CERT_VALIDATION</a> structure.

The <i>pConfigData</i> member is a pointer to a <a href="https://msdn.microsoft.com/1bc157c2-f3c2-4b67-a6ae-251ba1cb0379">WSD_SECURITY_CERT_VALIDATION</a> structure.

The <i>dwConfigDataSize</i> member is the size of the <a href="https://msdn.microsoft.com/1bc157c2-f3c2-4b67-a6ae-251ba1cb0379">WSD_SECURITY_CERT_VALIDATION</a> structure.


### -field WSD_SECURITY_SSL_NEGOTIATE_CLIENT_CERT

Specifies that on incoming SSL connections, WSDAPI  will request a client certificate from the SSL client if one is not already made available by the client.  If the remote entity cannot provide a client certificate, the connection will be rejected.  Note that the SSL record that is created for that port must expclicitly allow for client certificate negotiation.

The <i>pConfigData</i> member is <b>NULL</b>.

The <i>dwConfigDataSize</i> member is 0.


### -field WSD_SECURITY_COMPACTSIG_SIGNING_CERT

Used to specify which certificate is to be used by WSDAPI to sign outbound WS_Discovery UDP messages.

The <i>pConfigData</i> member is a                                            pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure  that represents the signing certificate.  The caller needs to have read access to the certificate's private key..

The <i>dwConfigDataSize</i> member is the size of the <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure.


### -field WSD_SECURITY_COMPACTSIG_VALIDATION

This is used to specify the parameters used to verify inbound signed WS_Discovery UDP message.

The <i>pConfigData</i> member is a                                            pointer to a <a href="https://msdn.microsoft.com/e2913f85-a5e7-43c9-a23c-81d836c9a259">WSD_SECURITY_SIGNATURE_VALIDATION</a> structure.

The <i>dwConfigDataSize</i> member is the size of the <a href="https://msdn.microsoft.com/e2913f85-a5e7-43c9-a23c-81d836c9a259">WSD_SECURITY_SIGNATURE_VALIDATION</a> structure.


### -field WSD_CONFIG_HOSTING_ADDRESSES

This applies only to the <a href="https://msdn.microsoft.com/2d2a78a2-fca6-4f54-9c75-3406a3c8d492">WSDCreateDeviceHost2</a> function.  It is used to specify an array of addresses on which the device host should be hosted on.  The equivalent is functionality provided through the <i>ppHostAddresses</i> and <i>dwHostAddressCount</i> parameters of the <a href="https://msdn.microsoft.com/8136fc01-9476-4ee4-aa44-784bef482ff5">WSDCreateDeviceHostAdvanced</a> function.

The <i>pConfigData</i> member is a                                            pointer to a <a href="https://msdn.microsoft.com/aaec97f4-c0b9-49d3-ab4c-758feda15d6a">WSD_CONFIG_ADDRESSES</a> structure.  The <b>addresses</b> member of this structure points to an array of <a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a> objects, each of which is an address on which the device host will listen on.

The <i>dwConfigDataSize</i> member is the size of the <a href="https://msdn.microsoft.com/aaec97f4-c0b9-49d3-ab4c-758feda15d6a">WSD_CONFIG_ADDRESSES</a> structure.


### -field WSD_CONFIG_DEVICE_ADDRESSES

This applies only to the <a href="https://msdn.microsoft.com/7b40a35d-f548-48fa-8ecd-3a0886a4c72a">WSDCreateDeviceProxy2</a> function.  It is used to specify an address for the device for which the proxy is created.  The equivalent is functionality provided through the <i>deviceConfig</i> parameter of the <a href="https://msdn.microsoft.com/31ddf62a-71d3-4f66-a704-2ee9e1fc8145">WSDCreateDeviceProxyAdvanced</a> function.

The <i>pConfigData</i> member is a                                            pointer to a <a href="https://msdn.microsoft.com/aaec97f4-c0b9-49d3-ab4c-758feda15d6a">WSD_CONFIG_ADDRESSES</a> structure.  The <b>addresses</b> member of this structure points to an array of <a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a> objects, each of which is an address of the device to which the proxy is created.  Currently only one such address is allowed.

The <i>dwConfigDataSize</i> member is the size of the <a href="https://msdn.microsoft.com/aaec97f4-c0b9-49d3-ab4c-758feda15d6a">WSD_CONFIG_ADDRESSES</a> structure.


### -field WSD_SECURITY_REQUIRE_HTTP_CLIENT_AUTH

Indicates a requirement for HTTP Authentication using one of the auth schemes specified through WSD_SECURITY_HTTP_AUTH_SCHEMES. Specific scenarios include:

<ul>
<li>
When specified during a <a href="https://msdn.microsoft.com/dbe7ccd0-494d-4f6c-90f6-e729839d7008">WSDCreateDeviceHost</a> operation, DPWS clients will be required to authenticate messages sent to the Hosted Services of the WSDAPI device host using HTTP Authentication.

</li>
<li>
If this is value is expressed in conjunction with WSD_SECURITY_SSL_NEGOTIATE_CLIENT_CERT, then WSDAPI will require HTTP clients to send a client certificate and utilize HTTP authentication. 

</li>
</ul>

### -field WSD_SECURITY_REQUIRE_CLIENT_CERT_OR_HTTP_CLIENT_AUTH

When this  value is specified, WSDAPI will request HTTP clients to send a client certificate. If the client cannot provide one, then WSDAPI will require  HTTP authentication. If the client can do neither, it will be rejected by WSDAPI. Specific scenarios include:

<ul>
<li>
When specified during a <a href="https://msdn.microsoft.com/dbe7ccd0-494d-4f6c-90f6-e729839d7008">WSDCreateDeviceHost</a> operation, this behavior will apply to web service messages from DPWS clients.

</li>
</ul>
<div class="alert"><b>Note</b>  This parameter cannot be used in conjunction with WSD_SECURITY_SSL_NEGOTIATE_CLIENT_CERT. If it is, WSDAPI will return E_INVALIDARG.</div>
<div> </div>

### -field WSD_SECURITY_USE_HTTP_CLIENT_AUTH

If the server requires authentication, WSDAPI will authenticate using HTTP authentication. Specific scenarios include:

<ul>
<li>
When specified during a <a href="https://msdn.microsoft.com/dbe7ccd0-494d-4f6c-90f6-e729839d7008">WSDCreateDeviceHost</a> operation, this behavior will apply to web service messages from DPWS clients.

</li>
<li>
If this value is expressed in conjunction with WSD_SECURITY_SSL_CERT_FOR_CLIENT_AUTH, WSDAPI will send the client certificate and authenticate using HTTP authentication if either operation is required by server.

</li>
</ul>
