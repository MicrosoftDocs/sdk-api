---
UID: NS:mschapp._ENCRYPTED_LM_OWF_PASSWORD
title: ENCRYPTED_LM_OWF_PASSWORD (mschapp.h)
description: The ENCRYPTED_LM_OWF_PASSWORD stores a user's encrypted Lan Manager (LM) one-way function (OWF) password hash.
helpviewer_keywords: ["*PENCRYPTED_LM_OWF_PASSWORD","*PENCRYPTED_NT_OWF_PASSWORD","ENCRYPTED_LM_OWF_PASSWORD","ENCRYPTED_LM_OWF_PASSWORD structure [MS-CHAP]","ENCRYPTED_NT_OWF_PASSWORD","mschap.encrypted_lm_owf_password","mschapp/ENCRYPTED_LM_OWF_PASSWORD"]
old-location: mschap\encrypted_lm_owf_password.htm
tech.root: MsChap
ms.assetid: 83498d3f-0ac5-435c-804e-a4baa1ae855d
ms.date: 12/05/2018
ms.keywords: '*PENCRYPTED_LM_OWF_PASSWORD, *PENCRYPTED_NT_OWF_PASSWORD, ENCRYPTED_LM_OWF_PASSWORD, ENCRYPTED_LM_OWF_PASSWORD structure [MS-CHAP], ENCRYPTED_NT_OWF_PASSWORD, mschap.encrypted_lm_owf_password, mschapp/ENCRYPTED_LM_OWF_PASSWORD'
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
req.typenames: ENCRYPTED_LM_OWF_PASSWORD, *PENCRYPTED_LM_OWF_PASSWORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENCRYPTED_LM_OWF_PASSWORD
 - mschapp/_ENCRYPTED_LM_OWF_PASSWORD
 - PENCRYPTED_LM_OWF_PASSWORD
 - mschapp/PENCRYPTED_LM_OWF_PASSWORD
 - ENCRYPTED_LM_OWF_PASSWORD
 - mschapp/ENCRYPTED_LM_OWF_PASSWORD
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
 - ENCRYPTED_LM_OWF_PASSWORD
---

# ENCRYPTED_LM_OWF_PASSWORD structure


## -description

The <b>ENCRYPTED_LM_OWF_PASSWORD</b> stores a user's encrypted Lan Manager (LM) one-way function (OWF) password hash.

## -struct-fields

### -field data

An array of <a href="/windows/desktop/api/mschapp/ns-mschapp-cypher_block">CYPHER_BLOCK</a> structures that contain an encrypted LM OWF password hash. The contents of the array are calculated using the <b>OldLmPasswordHashEncryptedWithNewNtPasswordHash()</b> function as defined in <a href="https://www.ietf.org/rfc/rfc2433.txt">RFC 2433</a>, section A.16.

## -remarks

<a href="/previous-versions/windows/desktop/legacy/cc325729(v=vs.85)">ENCRYPTED_NT_OWF_PASSWORD</a> is an alias for this structure.

## -see-also

<a href="/previous-versions/windows/desktop/mschap/ms-chap-password-management-structures">MS-CHAP Password Management Structures</a>



<a href="/previous-versions/windows/desktop/api/mschapp/nf-mschapp-mschapsrvchangepassword2">MSChapSrvChangePassword2</a>