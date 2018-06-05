---
UID: NS:webservices._WS_USERNAME_CREDENTIAL
title: "_WS_USERNAME_CREDENTIAL"
author: windows-sdk-content
description: The abstract base type for all username/password credentials.
old-location: wsw\ws_username_credential.htm
old-project: wsw
ms.assetid: 961f8c52-9922-4e43-905a-a22a80aba63b
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_USERNAME_CREDENTIAL, WS_USERNAME_CREDENTIAL structure [Web Services for Windows], _WS_USERNAME_CREDENTIAL, webservices/WS_USERNAME_CREDENTIAL, wsw.ws_username_credential
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WS_USERNAME_CREDENTIAL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_USERNAME_CREDENTIAL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_USERNAME_CREDENTIAL structure


## -description



The abstract base type for all username/password credentials.
            


Note that <b>WS_USERNAME_CREDENTIAL</b> and its concrete subtypes
are used with the WS-Security <a href="https://msdn.microsoft.com/be6d4787-fa50-4260-8236-39dd992adcae">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.  
They are best suitable for application-level username/password pairs, such as 
those used for online customer accounts.  The usernames and passwords specified 
are not interpreted by the security runtime, and are merely carried
client-to-server for authentication by the specified server-side
username/password validator specified by the application.
            


In contrast, the <a href="https://msdn.microsoft.com/78df2636-439b-4e55-8ca5-dc0f4f4ad745">WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a> and
its concrete subtypes are used for Windows Integrated Authentication
and the security bindings that use it.
            


## -struct-fields




### -field credentialType


The selector for the type of the username credential.
                

