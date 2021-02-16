---
UID: NS:wsman._WSMAN_USERNAME_PASSWORD_CREDS
title: WSMAN_USERNAME_PASSWORD_CREDS (wsman.h)
description: Defines the credentials used for authentication.
helpviewer_keywords: ["WSMAN_USERNAME_PASSWORD_CREDS","WSMAN_USERNAME_PASSWORD_CREDS structure [Windows Remote Management]","winrm.wsman_username_password_creds","wsman/WSMAN_USERNAME_PASSWORD_CREDS"]
old-location: winrm\wsman_username_password_creds.htm
tech.root: winrm
ms.assetid: 5cb2b52f-85a7-4760-9f0d-b515fad86d33
ms.date: 12/05/2018
ms.keywords: WSMAN_USERNAME_PASSWORD_CREDS, WSMAN_USERNAME_PASSWORD_CREDS structure [Windows Remote Management], winrm.wsman_username_password_creds, wsman/WSMAN_USERNAME_PASSWORD_CREDS
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
req.typenames: WSMAN_USERNAME_PASSWORD_CREDS
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_USERNAME_PASSWORD_CREDS
 - wsman/_WSMAN_USERNAME_PASSWORD_CREDS
 - WSMAN_USERNAME_PASSWORD_CREDS
 - wsman/WSMAN_USERNAME_PASSWORD_CREDS
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
 - WSMAN_USERNAME_PASSWORD_CREDS
---

# WSMAN_USERNAME_PASSWORD_CREDS structure


## -description

Defines the credentials used for authentication.

## -struct-fields

### -field username

Defines the user name for a local or domain account. It cannot be <b>NULL</b>.

### -field password

Defines the password for a local or domain account. It cannot be <b>NULL</b>.

## -remarks

The client can specify the credentials to use when creating a shell on a computer. The user name should be specified in the form DOMAIN\username for a domain account or SERVERNAME\username for a local account on a server computer.

If this structure is used, it should have both the user name and password fields specified. It can be used with Basic, Digest, Negotiate, or Kerberos authentication. The client must explicitly specify the credentials when either Basic or Digest authentication is used.

