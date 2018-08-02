---
UID: NS:wtsdefs._WTS_USER_CREDENTIAL
title: "_WTS_USER_CREDENTIAL"
author: windows-sdk-content
description: Contains credential information for a user.
old-location: termserv\wts_user_credential.htm
old-project: TermServ
ms.assetid: 79474bc1-3626-4c0e-ae63-6180404369ea
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PWTS_USER_CREDENTIAL, PWRDS_USER_CREDENTIAL, PWRDS_USER_CREDENTIAL structure pointer [Remote Desktop Services], PWTS_USER_CREDENTIAL, PWTS_USER_CREDENTIAL structure pointer [Remote Desktop Services], WRDS_USER_CREDENTIAL, WRDS_USER_CREDENTIAL structure [Remote Desktop Services], WTS_USER_CREDENTIAL, WTS_USER_CREDENTIAL structure [Remote Desktop Services], _WTS_USER_CREDENTIAL, termserv.wts_user_credential, wtsdefs/PWRDS_USER_CREDENTIAL, wtsdefs/PWTS_USER_CREDENTIAL, wtsdefs/WRDS_USER_CREDENTIAL, wtsdefs/WTS_USER_CREDENTIAL"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wtsdefs.h
req.include-header: Wtsprotocol.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
tech.root: 
req.typenames: WTS_USER_CREDENTIAL, *PWTS_USER_CREDENTIAL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsdefs.h
api_name:
 - WTS_USER_CREDENTIAL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WTS_USER_CREDENTIAL structure


## -description


Contains credential information for a user. This structure is used by the <a href="https://msdn.microsoft.com/48cd1a57-5f6d-4feb-889d-7441a76c0410">GetUserCredentials</a> method.


## -struct-fields




### -field UserName

A string that contains the name of the user.


### -field Password

A string that contains the user password.


### -field Domain

A string that contains the domain name for the user.


## -remarks



The user name and password are plaintext.



