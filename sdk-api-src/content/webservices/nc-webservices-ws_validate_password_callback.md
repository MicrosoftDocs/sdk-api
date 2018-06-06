---
UID: NC:webservices.WS_VALIDATE_PASSWORD_CALLBACK
title: WS_VALIDATE_PASSWORD_CALLBACK
author: windows-sdk-content
description: Validates a username/password pair on the receiver side.
old-location: wsw\ws_validate_password_callback.htm
old-project: wsw
ms.assetid: 3cf8f2a1-61b4-4702-954e-e5eb260820c7
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_VALIDATE_PASSWORD_CALLBACK, WS_VALIDATE_PASSWORD_CALLBACK callback, WS_VALIDATE_PASSWORD_CALLBACK callback function [Web Services for Windows], webservices/WS_VALIDATE_PASSWORD_CALLBACK, wsw.ws_validate_password_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WebServices.h
api_name:
 - WS_VALIDATE_PASSWORD_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_VALIDATE_PASSWORD_CALLBACK callback function


## -description



Validates a username/password pair
on the receiver side.  When a <a href="https://msdn.microsoft.com/be6d4787-fa50-4260-8236-39dd992adcae">WS_USERNAME_MESSAGE_SECURITY_BINDING</a> 
containing this callback is included in the security description, this callback
is invoked for each received message at the server.  This callback is expected 
to return S_OKif the username/password pair was successfully validated, S_FALSE 
when the pair could not be validated and an error value if an unexpected error occurred.
Returning any result other than S_OK from this callback will result in
the associated receive message failing with a security error.
            


As with all security callbacks, the application should expect to
receive this callback any time between channel/listener open and close,
but it will never be invoked when a channel is not open.  In the
current drop, this callback is always invoked synchronously.  In the
next drop, this callback will be invoked synchronously for synchronous
message receives and asynchronously for asynchronous message receives,
but it will always be invoked <a href="https://msdn.microsoft.com/6a8e4c0b-3c0a-4bd3-bbac-40e6f499a055">short</a>
when it is invoked asynchronously.
            


## -parameters




### -param *passwordValidatorCallbackState [in, optional]


The state to be passed back when invoking this callback.
                


### -param *username [in]


Received username.
                


### -param *password [in]


Received password.
                


### -param *asyncContext [in, optional]


Information on how to invoke the function asynchronously, or <b>NULL</b> if invoking synchronously.
                


### -param *error [in, optional]


Specifies where additional error information should be stored if the function fails.
                


## -returns



This callback function does not return a value.



