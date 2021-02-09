---
UID: NC:webservices.WS_GET_CERT_CALLBACK
title: WS_GET_CERT_CALLBACK (webservices.h)
description: Provides a certificate to the security runtime.
helpviewer_keywords: ["WS_GET_CERT_CALLBACK","WS_GET_CERT_CALLBACK callback","WS_GET_CERT_CALLBACK callback function [Web Services for Windows]","webservices/WS_GET_CERT_CALLBACK","wsw.ws_get_cert_callback"]
old-location: wsw\ws_get_cert_callback.htm
tech.root: wsw
ms.assetid: 36e787ff-f6bc-4814-be3f-a64f3edc2326
ms.date: 12/05/2018
ms.keywords: WS_GET_CERT_CALLBACK, WS_GET_CERT_CALLBACK callback, WS_GET_CERT_CALLBACK callback function [Web Services for Windows], webservices/WS_GET_CERT_CALLBACK, wsw.ws_get_cert_callback
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - WS_GET_CERT_CALLBACK
 - webservices/WS_GET_CERT_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_GET_CERT_CALLBACK
---

# WS_GET_CERT_CALLBACK callback function


## -description

Provides a certificate to the security runtime.  This
callback is specified as part of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_custom_cert_credential">WS_CUSTOM_CERT_CREDENTIAL</a>, 
which in turn may be specified as part of a security binding that requires a 
certificate credential. The runtime will invoke this callback when the channel 
(client-side) or the listener (server-side) is opened.
            

Cert ownership: If this callback returns a success HRESULT, the caller
(namely, the security runtime) will take ownership of the returned
certificate, and will free it when the containing channel no longer
needs it.  If this callback returns a failure HRESULT, the caller will
NOT take ownership of, or even look at, the value returned in the out
parameter 'cert'.

## -parameters

### -param getCertCallbackState [in]

State that was specified along with this callback in the certificate credential.

### -param targetAddress [in, optional]

The target address to whom this certificate is to be presented, in
case this certificate credential is specified for a client.

### -param viaUri [in, optional]

The via address to whom this certificate is to be presented.
                


#### - **cert

The location to return the certificate.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

### -param cert

The location to return the certificate.

## -returns

This callback function does not return a value.
