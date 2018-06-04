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

# WS_GET_CERT_CALLBACK callback function


## -description


Provides a certificate to the security runtime.  This
callback is specified as part of the <a href="https://msdn.microsoft.com/822dd067-803c-4e72-bfd0-fd9f9f36d390">WS_CUSTOM_CERT_CREDENTIAL</a>, 
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




### -param *getCertCallbackState [in]


State that was specified along with this callback in the certificate credential.
                


### -param *targetAddress [in, optional]


The target address to whom this certificate is to be presented, in
case this certificate credential is specified for a client.
                


### -param *viaUri [in, optional]


The via address to whom this certificate is to be presented.
                


#### - **cert


The location to return the certificate.
                


### -param *error [in, optional]


Specifies where additional error information should be stored if the function fails.
                


#### - cert


The location to return the certificate.
                


## -returns



This callback function does not return a value.



