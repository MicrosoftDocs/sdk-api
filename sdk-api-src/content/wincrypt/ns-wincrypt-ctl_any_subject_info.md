---
UID: NS:wincrypt._CTL_ANY_SUBJECT_INFO
title: CTL_ANY_SUBJECT_INFO (wincrypt.h)
description: Contains a SubjectAlgorithm to be matched in the certificate trust list (CTL) and the SubjectIdentifier to be matched in one of the CTL entries in calls to CertFindSubjectInCTL.
helpviewer_keywords: ["*PCTL_ANY_SUBJECT_INFO","CTL_ANY_SUBJECT_INFO","CTL_ANY_SUBJECT_INFO structure [Security]","PCTL_ANY_SUBJECT_INFO","PCTL_ANY_SUBJECT_INFO structure pointer [Security]","_crypto2_ctl_any_subject_info","security.ctl_any_subject_info","wincrypt/CTL_ANY_SUBJECT_INFO","wincrypt/PCTL_ANY_SUBJECT_INFO"]
old-location: security\ctl_any_subject_info.htm
tech.root: security
ms.assetid: 367e9914-b69b-47ad-a20a-3dd067708787
ms.date: 12/05/2018
ms.keywords: '*PCTL_ANY_SUBJECT_INFO, CTL_ANY_SUBJECT_INFO, CTL_ANY_SUBJECT_INFO structure [Security], PCTL_ANY_SUBJECT_INFO, PCTL_ANY_SUBJECT_INFO structure pointer [Security], _crypto2_ctl_any_subject_info, security.ctl_any_subject_info, wincrypt/CTL_ANY_SUBJECT_INFO, wincrypt/PCTL_ANY_SUBJECT_INFO'
req.header: wincrypt.h
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
req.typenames: CTL_ANY_SUBJECT_INFO, *PCTL_ANY_SUBJECT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CTL_ANY_SUBJECT_INFO
 - wincrypt/_CTL_ANY_SUBJECT_INFO
 - PCTL_ANY_SUBJECT_INFO
 - wincrypt/PCTL_ANY_SUBJECT_INFO
 - CTL_ANY_SUBJECT_INFO
 - wincrypt/CTL_ANY_SUBJECT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CTL_ANY_SUBJECT_INFO
---

# CTL_ANY_SUBJECT_INFO structure


## -description

The <b>CTL_ANY_SUBJECT_INFO</b> structure contains a <b>SubjectAlgorithm</b> to be matched in the <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) and the <b>SubjectIdentifier</b> to be matched in one of the CTL entries in calls to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindsubjectinctl">CertFindSubjectInCTL</a>.

## -struct-fields

### -field SubjectAlgorithm

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure containing the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) of an algorithm type and any associated additional parameters. The <b>pszObjId</b> can be set to <b>NULL</b> to exclude a <b>SubjectAlgorithm</b> comparison.

### -field SubjectIdentifier

<a href="/windows/desktop/SecGloss/b-gly">BLOB</a> containing a unique identifier of the subject.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_subject_para">CTL_FIND_SUBJECT_PARA</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindctlinstore">CertFindCTLInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindsubjectinctl">CertFindSubjectInCTL</a>