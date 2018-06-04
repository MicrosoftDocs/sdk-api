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



