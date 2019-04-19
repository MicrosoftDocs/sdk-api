---
UID: NS:webservices._WS_USERNAME_CREDENTIAL
title: WS_USERNAME_CREDENTIAL (webservices.h)
author: windows-sdk-content
description: The abstract base type for all username/password credentials.
old-location: wsw\ws_username_credential.htm
tech.root: wsw
ms.assetid: 961f8c52-9922-4e43-905a-a22a80aba63b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WS_USERNAME_CREDENTIAL, WS_USERNAME_CREDENTIAL structure [Web Services for Windows], webservices/WS_USERNAME_CREDENTIAL, wsw.ws_username_credential
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
 - WS_USERNAME_CREDENTIAL
product: Windows
targetos: Windows
req.typenames: WS_USERNAME_CREDENTIAL
req.redist: 
ms.custom: 19H1
---

# WS_USERNAME_CREDENTIAL structure


## -description


The abstract base type for all username/password credentials.
            

Note that <b>WS_USERNAME_CREDENTIAL</b> and its concrete subtypes
are used with the WS-Security <a href="https://msdn.microsoft.com/en-us/library/Dd323497(v=VS.85).aspx">WS_USERNAME_MESSAGE_SECURITY_BINDING</a>.  
They are best suitable for application-level username/password pairs, such as 
those used for online customer accounts.  The usernames and passwords specified 
are not interpreted by the security runtime, and are merely carried
client-to-server for authentication by the specified server-side
username/password validator specified by the application.
            

In contrast, the <a href="https://msdn.microsoft.com/en-us/library/Dd323506(v=VS.85).aspx">WS_WINDOWS_INTEGRATED_AUTH_CREDENTIAL</a> and
its concrete subtypes are used for Windows Integrated Authentication
and the security bindings that use it.
            


## -struct-fields




### -field credentialType

The selector for the type of the username credential.
                

