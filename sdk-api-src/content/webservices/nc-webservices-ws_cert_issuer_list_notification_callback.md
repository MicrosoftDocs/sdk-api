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

# WS_CERT_ISSUER_LIST_NOTIFICATION_CALLBACK callback function


## -description


Notifies the client of the list of certificate issuers
that are acceptable to the server.  With some protocols such as SSL,
the server may optionally send such an issuer list to help the client
choose a certificate.
            


This callback is an optional part of the <a href="https://msdn.microsoft.com/822dd067-803c-4e72-bfd0-fd9f9f36d390">WS_CUSTOM_CERT_CREDENTIAL</a>.  
If the (possibly <b>NULL</b>) certificate returned by the <a href="https://msdn.microsoft.com/36e787ff-f6bc-4814-be3f-a64f3edc2326">WS_GET_CERT_CALLBACK</a> is
accepted by the server, then this callback is never invoked.  If the
server rejects it and sends back an issuer list, then this callback
will be invoked.  The client may then choose a certificate based on
the issuer list and supply that certificate when the channel is opened
next and <i>WS_GET_CERT_CALLBACK</i> is invoked again.
            


The parameters supplied during this callback are valid only for the
duration of the callback.
            


## -parameters




### -param *certIssuerListNotificationCallbackState [in]


State that was specified along with this callback in the <a href="https://msdn.microsoft.com/822dd067-803c-4e72-bfd0-fd9f9f36d390">WS_CUSTOM_CERT_CREDENTIAL</a>.
                


### -param *issuerList [in]


The list of certificate issuers acceptable to the server.
                


### -param *error [in, optional]


Specifies where additional error information should be stored if the function fails.
                


## -returns



This callback function does not return a value.



