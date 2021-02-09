---
UID: NC:webservices.WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK
title: WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK (webservices.h)
description: Notifies the client of the list of certificate issuers that are acceptable to the server.
helpviewer_keywords: ["WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK","WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK callback","WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK callback function [Web Services for Windows]","webservices/WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK","wsw.ws_cert_issuer_list_notification_callback"]
old-location: wsw\ws_cert_issuer_list_notification_callback.htm
tech.root: wsw
ms.assetid: a8417d3f-5932-4993-b206-b43b6a93ef8f
ms.date: 12/05/2018
ms.keywords: WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK, WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK callback, WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK callback function [Web Services for Windows], webservices/WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK, wsw.ws_cert_issuer_list_notification_callback
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
 - WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK
 - webservices/WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK
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
 - WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK
---

# WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK callback function


## -description

Notifies the client of the list of certificate issuers
that are acceptable to the server.  With some protocols such as SSL,
the server may optionally send such an issuer list to help the client
choose a certificate.
            

This callback is an optional part of the <a href="/windows/desktop/api/webservices/ns-webservices-ws_custom_cert_credential">WS_CUSTOM_CERT_CREDENTIAL</a>.  
If the (possibly <b>NULL</b>) certificate returned by the <a href="/windows/desktop/api/webservices/nc-webservices-ws_get_cert_callback">WS_GET_CERT_CALLBACK</a> is
accepted by the server, then this callback is never invoked.  If the
server rejects it and sends back an issuer list, then this callback
will be invoked.  The client may then choose a certificate based on
the issuer list and supply that certificate when the channel is opened
next and <i>WS_GET_CERT_CALLBACK</i> is invoked again.
            

The parameters supplied during this callback are valid only for the
duration of the callback.

## -parameters

### -param certIssuerListNotificationCallbackState [in]

State that was specified along with this callback in the <a href="/windows/desktop/api/webservices/ns-webservices-ws_custom_cert_credential">WS_CUSTOM_CERT_CREDENTIAL</a>.

### -param issuerList [in]

The list of certificate issuers acceptable to the server.

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

## -returns

This callback function does not return a value.
