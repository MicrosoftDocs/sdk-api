---
UID: NS:webservices._WS_CUSTOM_CERT_CREDENTIAL
title: WS_CUSTOM_CERT_CREDENTIAL
author: windows-sdk-content
description: The type for specifying a certificate credential that is to be supplied by a callback to the application.
old-location: wsw\ws_custom_cert_credential.htm
tech.root: wsw
ms.assetid: 822dd067-803c-4e72-bfd0-fd9f9f36d390
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_CUSTOM_CERT_CREDENTIAL, WS_CUSTOM_CERT_CREDENTIAL structure [Web Services for Windows], webservices/WS_CUSTOM_CERT_CREDENTIAL, wsw.ws_custom_cert_credential
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_CUSTOM_CERT_CREDENTIAL
product: Windows
targetos: Windows
req.typenames: WS_CUSTOM_CERT_CREDENTIAL
req.redist: 
---

# WS_CUSTOM_CERT_CREDENTIAL structure


## -description


The type for specifying a certificate credential that is to be
supplied by a callback to the application.  This callback is invoked
to get the certificate during <a href="https://msdn.microsoft.com/a7226194-0974-4f3c-b92d-78a93e86eea5">WsOpenChannel</a> on the client
side and during <a href="https://msdn.microsoft.com/36226881-3fe7-4510-b147-7ee30146482c">WsOpenListener</a> on the server side.  It is
always invoked <a href="https://msdn.microsoft.com/6a8e4c0b-3c0a-4bd3-bbac-40e6f499a055">short</a>.
            


## -struct-fields




### -field credential

The base type from which this type and all other certificate credential types derive.
                


### -field getCertCallback

The Callback to get the certificate.
                


### -field getCertCallbackState

The state to be passed when invoking the callback.
                


### -field certIssuerListNotificationCallback

 


### -field certIssuerListNotificationCallbackState

 



