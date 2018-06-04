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

# WS_VALIDATE_SAML_CALLBACK callback function


## -description


Validates a SAML assertion.  If a
received SAML assertion passes the signature verification checks that
ensure the SAML was issued by a trusted issuer, then this callback is
invoked to enable the application to do additional validation on the
XML form of the SAML assertion.  This callback is expected to return
S_OK if the SAML assertion was successfully validated, S_FALSE when
the assertion could not be validated and an error value if an
unexpected error occurred.  Returning any result other than S_OK from
this callback will result in the associated receive message failing
with a security error.
            


As with all security callbacks, the application should expect to
receive this callback any time between listener open and close, but it
will never be invoked when a listener is not open.
            


## -parameters




### -param *samlValidatorCallbackState [in, optional]


The state to be passed back when invoking this callback.
                


### -param *samlAssertion [in]


The received SAML assertion that has undergone a successful signature check.
                


### -param *error [in, optional]


Specifies where additional error information should be stored if the function fails.
                


## -returns



This callback function does not return a value.



