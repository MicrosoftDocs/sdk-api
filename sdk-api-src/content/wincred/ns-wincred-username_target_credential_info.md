---
UID: NS:wincred._USERNAME_TARGET_CREDENTIAL_INFO
title: USERNAME_TARGET_CREDENTIAL_INFO (wincred.h)
description: The USERNAME_TARGET_CREDENTIAL_INFO structure contains a reference to a credential.
helpviewer_keywords: ["*PUSERNAME_TARGET_CREDENTIAL_INFO","PUSERNAME_TARGET_CREDENTIAL_INFO","PUSERNAME_TARGET_CREDENTIAL_INFO structure pointer [Security]","USERNAME_TARGET_CREDENTIAL_INFO","USERNAME_TARGET_CREDENTIAL_INFO structure [Security]","_cred_username_target_credential_info","security.username_target_credential_info","wincred/PUSERNAME_TARGET_CREDENTIAL_INFO","wincred/USERNAME_TARGET_CREDENTIAL_INFO"]
old-location: security\username_target_credential_info.htm
tech.root: security
ms.assetid: 1cb56a85-fafd-4471-b0e9-660ac0dc0219
ms.date: 12/05/2018
ms.keywords: '*PUSERNAME_TARGET_CREDENTIAL_INFO, PUSERNAME_TARGET_CREDENTIAL_INFO, PUSERNAME_TARGET_CREDENTIAL_INFO structure pointer [Security], USERNAME_TARGET_CREDENTIAL_INFO, USERNAME_TARGET_CREDENTIAL_INFO structure [Security], _cred_username_target_credential_info, security.username_target_credential_info, wincred/PUSERNAME_TARGET_CREDENTIAL_INFO, wincred/USERNAME_TARGET_CREDENTIAL_INFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _USERNAME_TARGET_CREDENTIAL_INFO
 - wincred/_USERNAME_TARGET_CREDENTIAL_INFO
 - PUSERNAME_TARGET_CREDENTIAL_INFO
 - wincred/PUSERNAME_TARGET_CREDENTIAL_INFO
 - USERNAME_TARGET_CREDENTIAL_INFO
 - wincred/USERNAME_TARGET_CREDENTIAL_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinCred.h
api_name:
 - USERNAME_TARGET_CREDENTIAL_INFO
---

# USERNAME_TARGET_CREDENTIAL_INFO structure


## -description

The 
<b>USERNAME_TARGET_CREDENTIAL_INFO</b> structure contains a reference to a credential. This structure is used to pass a user name into the 
<a href="/windows/desktop/api/wincred/nf-wincred-credmarshalcredentiala">CredMarshalCredential</a> function and out of the 
<a href="/windows/desktop/api/wincred/nf-wincred-credunmarshalcredentiala">CredUnmarshalCredential</a>. The resultant marshaled credential can be passed as the <i>lpszUserName</i> parameter of the <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> function to direct that API to get the password from the corresponding CRED_FLAGS_USERNAME_TARGET credential instead of from the <i>lpszPassword</i> parameter of the function.

## -struct-fields

### -field UserName

 User name of the USERNAME_TARGET_CREDENTIAL_INFO credential.