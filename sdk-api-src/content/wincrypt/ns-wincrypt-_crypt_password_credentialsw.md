---
UID: NS:wincrypt._CRYPT_PASSWORD_CREDENTIALSW
title: "_CRYPT_PASSWORD_CREDENTIALSW"
author: windows-sdk-content
description: Contains the user name and password credentials to be used in the CRYPT_CREDENTIALS structure as optional input to a remote object retrieval function such as CryptRetrieveObjectByUrl or CryptGetTimeValidObject.
old-location: security\crypt_password_credentials.htm
tech.root: seccrypto
ms.assetid: 21461344-1080-4603-bda1-a92dfda68c15
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PCRYPT_PASSWORD_CREDENTIALSW, CRYPT_PASSWORD_CREDENTIALS, CRYPT_PASSWORD_CREDENTIALS structure [Security], CRYPT_PASSWORD_CREDENTIALSA, CRYPT_PASSWORD_CREDENTIALSW, PCRYPT_PASSWORD_CREDENTIALS, PCRYPT_PASSWORD_CREDENTIALS structure pointer [Security], _CRYPT_PASSWORD_CREDENTIALSW, security.crypt_password_credentials, wincrypt/CRYPT_PASSWORD_CREDENTIALS, wincrypt/CRYPT_PASSWORD_CREDENTIALSA, wincrypt/CRYPT_PASSWORD_CREDENTIALSW, wincrypt/PCRYPT_PASSWORD_CREDENTIALS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CRYPT_PASSWORD_CREDENTIALSW (Unicode) and CRYPT_PASSWORD_CREDENTIALSA (ANSI)
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
 - WinCrypt.h
api_name:
 - CRYPT_PASSWORD_CREDENTIALS
 - CRYPT_PASSWORD_CREDENTIALSA
 - CRYPT_PASSWORD_CREDENTIALSW
product: Windows
targetos: Windows
req.typenames: CRYPT_PASSWORD_CREDENTIALSW, *PCRYPT_PASSWORD_CREDENTIALSW
req.redist: 
---

# _CRYPT_PASSWORD_CREDENTIALSW structure


## -description


The <b>CRYPT_PASSWORD_CREDENTIALS</b> structure contains the user name and password credentials to be used in the <a href="https://msdn.microsoft.com/d28b2f52-3258-44ad-a3ab-0743d3afcd62">CRYPT_CREDENTIALS</a> structure as optional input to a remote object retrieval function such as <a href="https://msdn.microsoft.com/2e205f97-be9b-4358-ba22-d475b6a250b7">CryptRetrieveObjectByUrl</a> or <a href="https://msdn.microsoft.com/dd639b43-1560-4e9f-a778-9e20484ae012">CryptGetTimeValidObject</a>.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field pszUsername

A pointer to a null-terminated string that contains the user name credential for the remote session authentication.


### -field pszPassword

A pointer to a null-terminated string that contains the password credential for the remote session authentication.

