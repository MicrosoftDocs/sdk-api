---
UID: NS:mschapp._SAMPR_ENCRYPTED_USER_PASSWORD
title: SAMPR_ENCRYPTED_USER_PASSWORD (mschapp.h)
description: The SAMPR_ENCRYPTED_USER_PASSWORD stores a user's encrypted password.
helpviewer_keywords: ["*PSAMPR_ENCRYPTED_USER_PASSWORD","*PSAMPR_ENCRYPTED_USER_PASSWORD structure [MS-CHAP]","SAMPR_ENCRYPTED_USER_PASSWORD","SAMPR_ENCRYPTED_USER_PASSWORD structure [MS-CHAP]","mschap.sampr_encrypted_user_password","mschapp/*PSAMPR_ENCRYPTED_USER_PASSWORD","mschapp/SAMPR_ENCRYPTED_USER_PASSWORD"]
old-location: mschap\sampr_encrypted_user_password.htm
tech.root: MsChap
ms.assetid: 10137c59-db99-4d70-9716-6f05369084a0
ms.date: 12/05/2018
ms.keywords: '*PSAMPR_ENCRYPTED_USER_PASSWORD, *PSAMPR_ENCRYPTED_USER_PASSWORD structure [MS-CHAP], SAMPR_ENCRYPTED_USER_PASSWORD, SAMPR_ENCRYPTED_USER_PASSWORD structure [MS-CHAP], mschap.sampr_encrypted_user_password, mschapp/*PSAMPR_ENCRYPTED_USER_PASSWORD, mschapp/SAMPR_ENCRYPTED_USER_PASSWORD'
req.header: mschapp.h
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
req.typenames: SAMPR_ENCRYPTED_USER_PASSWORD, *PSAMPR_ENCRYPTED_USER_PASSWORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SAMPR_ENCRYPTED_USER_PASSWORD
 - mschapp/_SAMPR_ENCRYPTED_USER_PASSWORD
 - PSAMPR_ENCRYPTED_USER_PASSWORD
 - mschapp/PSAMPR_ENCRYPTED_USER_PASSWORD
 - SAMPR_ENCRYPTED_USER_PASSWORD
 - mschapp/SAMPR_ENCRYPTED_USER_PASSWORD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MsChapp.h
api_name:
 - SAMPR_ENCRYPTED_USER_PASSWORD
---

# SAMPR_ENCRYPTED_USER_PASSWORD structure


## -description

The <b>SAMPR_ENCRYPTED_USER_PASSWORD</b> stores a user's encrypted password.

## -struct-fields

### -field Buffer

An array contains an encrypted password. The contents of the array are calculated using either the <b>NewPasswordEncryptedWithOldNtPasswordHash</b> or <b>NewPasswordEncryptedWithOldLmPasswordHash</b> functions as defined in <a href="https://www.ietf.org/rfc/rfc2433.txt">RFC 2433</a>, sections A.11 and A.15 respectively.

## -see-also

<a href="/previous-versions/windows/desktop/mschap/ms-chap-password-management-structures">MS-CHAP Password Management Structures</a>



<a href="/previous-versions/windows/desktop/api/mschapp/nf-mschapp-mschapsrvchangepassword2">MSChapSrvChangePassword2</a>