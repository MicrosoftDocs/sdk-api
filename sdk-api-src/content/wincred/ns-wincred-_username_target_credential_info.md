---
UID: NS:wincred._USERNAME_TARGET_CREDENTIAL_INFO
title: "_USERNAME_TARGET_CREDENTIAL_INFO"
author: windows-driver-content
description: The USERNAME_TARGET_CREDENTIAL_INFO structure contains a reference to a credential.
old-location: security\username_target_credential_info.htm
old-project: SecAuthN
ms.assetid: 1cb56a85-fafd-4471-b0e9-660ac0dc0219
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PUSERNAME_TARGET_CREDENTIAL_INFO, PUSERNAME_TARGET_CREDENTIAL_INFO, PUSERNAME_TARGET_CREDENTIAL_INFO structure pointer [Security], USERNAME_TARGET_CREDENTIAL_INFO, USERNAME_TARGET_CREDENTIAL_INFO structure [Security], _USERNAME_TARGET_CREDENTIAL_INFO, _cred_username_target_credential_info, security.username_target_credential_info, wincred/PUSERNAME_TARGET_CREDENTIAL_INFO, wincred/USERNAME_TARGET_CREDENTIAL_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinCred.h
api_name:
-	USERNAME_TARGET_CREDENTIAL_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _USERNAME_TARGET_CREDENTIAL_INFO structure


## -description


The 
<b>USERNAME_TARGET_CREDENTIAL_INFO</b> structure contains a reference to a credential. This structure is used to pass a user name into the 
<a href="https://msdn.microsoft.com/20a1d54b-04a7-4b0a-88e4-1970d1f71502">CredMarshalCredential</a> function and out of the 
<a href="https://msdn.microsoft.com/65757235-d92c-479f-8e2b-1f8d8564792b">CredUnmarshalCredential</a>. The resultant marshaled credential can be passed as the <i>lpszUserName</i> parameter of the <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> function to direct that API to get the password from the corresponding CRED_FLAGS_USERNAME_TARGET credential instead of from the <i>lpszPassword</i> parameter of the function.


## -struct-fields




### -field UserName

 User name of the USERNAME_TARGET_CREDENTIAL_INFO credential.

