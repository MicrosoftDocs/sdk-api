---
UID: NS:wsman._WSMAN_AUTHENTICATION_CREDENTIALS
title: "_WSMAN_AUTHENTICATION_CREDENTIALS"
author: windows-sdk-content
description: Defines the authentication method and the credentials used for server or proxy authentication.
old-location: winrm\wsman_authentication_credentials.htm
old-project: WinRM
ms.assetid: e9090d88-c76e-4a85-946e-ff46403e6725
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSMAN_AUTHENTICATION_CREDENTIALS, WSMAN_AUTHENTICATION_CREDENTIALS structure [Windows Remote Management], _WSMAN_AUTHENTICATION_CREDENTIALS, winrm.wsman_authentication_credentials, wsman/WSMAN_AUTHENTICATION_CREDENTIALS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSMAN_AUTHENTICATION_CREDENTIALS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wsman.h
api_name:
-	WSMAN_AUTHENTICATION_CREDENTIALS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSMAN_AUTHENTICATION_CREDENTIALS structure


## -description


Defines the authentication method and the credentials used for server or proxy authentication.


## -struct-fields




### -field authenticationMechanism

Defines the authentication mechanism. This member can be set to zero. If it is set to zero, the WinRM client will choose between Kerberos and Negotiate. If it is not set to zero, this member must be one of the values of the <a href="https://msdn.microsoft.com/ce5ddaf6-4d81-4dab-a928-819b1fdee6c8">WSManAuthenticationFlags</a> enumeration.


### -field userAccount

Defines the credentials used for authentication. See <a href="https://msdn.microsoft.com/5cb2b52f-85a7-4760-9f0d-b515fad86d33">WSMAN_USERNAME_PASSWORD_CREDS</a> for more information.


### -field certificateThumbprint

Defines the certificate thumbprint.

