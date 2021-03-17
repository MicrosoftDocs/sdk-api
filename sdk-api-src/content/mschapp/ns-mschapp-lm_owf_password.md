---
UID: NS:mschapp._LM_OWF_PASSWORD
title: LM_OWF_PASSWORD (mschapp.h)
description: The LM_OWF_PASSWORD stores the Lan Manage (LM) one-way function (OWF) of a user's password.
helpviewer_keywords: ["*PLM_OWF_PASSWORD","*PNT_OWF_PASSWORD","LM_OWF_PASSWORD","LM_OWF_PASSWORD structure [MS-CHAP]","NT_OWF_PASSWORD","PLM_OWF_PASSWORD","PLM_OWF_PASSWORD structure pointer [MS-CHAP]","_LM_OWF_PASSWORD","mschap.lm_owf_password","mschapp/LM_OWF_PASSWORD","mschapp/PLM_OWF_PASSWORD"]
old-location: mschap\lm_owf_password.htm
tech.root: MsChap
ms.assetid: db155f34-fa57-4449-9319-d46561fd18c0
ms.date: 12/05/2018
ms.keywords: '*PLM_OWF_PASSWORD, *PNT_OWF_PASSWORD, LM_OWF_PASSWORD, LM_OWF_PASSWORD structure [MS-CHAP], NT_OWF_PASSWORD, PLM_OWF_PASSWORD, PLM_OWF_PASSWORD structure pointer [MS-CHAP], _LM_OWF_PASSWORD, mschap.lm_owf_password, mschapp/LM_OWF_PASSWORD, mschapp/PLM_OWF_PASSWORD'
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
req.typenames: LM_OWF_PASSWORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LM_OWF_PASSWORD
 - mschapp/_LM_OWF_PASSWORD
 - LM_OWF_PASSWORD
 - mschapp/LM_OWF_PASSWORD
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
 - LM_OWF_PASSWORD
---

# LM_OWF_PASSWORD structure


## -description

The <b>LM_OWF_PASSWORD</b> stores the Lan Manage (LM) one-way function (OWF) of a user's password.

## -struct-fields

### -field data

An array of <a href="/windows/desktop/api/mschapp/ns-mschapp-cypher_block">CYPHER_BLOCK</a> structures that contain a LM OWF password hash. The contents of the array are calculated using the <b>LmEncryptedPasswordHash()</b> function as defined in <a href="https://www.ietf.org/rfc/rfc2433.txt">RFC 2433</a>, section A.8.

## -remarks

<a href="/previous-versions/windows/desktop/legacy/cc325731(v=vs.85)">NT_OWF_PASSWORD</a> is an alias for this structure.

## -see-also

<a href="/previous-versions/windows/desktop/mschap/ms-chap-password-management-structures">MS-CHAP Password Management Structures</a>



<a href="/previous-versions/windows/desktop/api/mschapp/nf-mschapp-mschapsrvchangepassword">MSChapSrvChangePassword</a>