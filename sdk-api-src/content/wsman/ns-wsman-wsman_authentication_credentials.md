---
UID: NS:wsman._WSMAN_AUTHENTICATION_CREDENTIALS
title: WSMAN_AUTHENTICATION_CREDENTIALS (wsman.h)
description: Defines the authentication method and the credentials used for server or proxy authentication.
helpviewer_keywords: ["WSMAN_AUTHENTICATION_CREDENTIALS","WSMAN_AUTHENTICATION_CREDENTIALS structure [Windows Remote Management]","winrm.wsman_authentication_credentials","wsman/WSMAN_AUTHENTICATION_CREDENTIALS"]
old-location: winrm\wsman_authentication_credentials.htm
tech.root: winrm
ms.assetid: e9090d88-c76e-4a85-946e-ff46403e6725
ms.date: 12/05/2018
ms.keywords: WSMAN_AUTHENTICATION_CREDENTIALS, WSMAN_AUTHENTICATION_CREDENTIALS structure [Windows Remote Management], winrm.wsman_authentication_credentials, wsman/WSMAN_AUTHENTICATION_CREDENTIALS
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSMAN_AUTHENTICATION_CREDENTIALS
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_AUTHENTICATION_CREDENTIALS
 - wsman/_WSMAN_AUTHENTICATION_CREDENTIALS
 - WSMAN_AUTHENTICATION_CREDENTIALS
 - wsman/WSMAN_AUTHENTICATION_CREDENTIALS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_AUTHENTICATION_CREDENTIALS
---

# WSMAN_AUTHENTICATION_CREDENTIALS structure


## -description

Defines the authentication method and the credentials used for server or proxy authentication.

## -struct-fields

### -field authenticationMechanism

Defines the authentication mechanism. This member can be set to zero. If it is set to zero, the WinRM client will choose between Kerberos and Negotiate. If it is not set to zero, this member must be one of the values of the <a href="/windows/desktop/api/wsman/ne-wsman-wsmanauthenticationflags">WSManAuthenticationFlags</a> enumeration.

### -field userAccount

Defines the credentials used for authentication. See <a href="/windows/desktop/api/wsman/ns-wsman-wsman_username_password_creds">WSMAN_USERNAME_PASSWORD_CREDS</a> for more information.

### -field certificateThumbprint

Defines the certificate thumbprint.