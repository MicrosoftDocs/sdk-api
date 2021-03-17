---
UID: NS:wincrypt._CTL_FIND_SUBJECT_PARA
title: CTL_FIND_SUBJECT_PARA (wincrypt.h)
description: Contains data used by CertFindCTLInStore with a dwFindType parameter of CTL_FIND_SUBJECT to find a Certificate Trust List (CTL).
helpviewer_keywords: ["*PCTL_FIND_SUBJECT_PARA","CTL_FIND_SUBJECT_PARA","CTL_FIND_SUBJECT_PARA structure [Security]","PCTL_FIND_SUBJECT_PARA","PCTL_FIND_SUBJECT_PARA structure pointer [Security]","_crypto2_ctl_find_subject_para","security.ctl_find_subject_para","wincrypt/CTL_FIND_SUBJECT_PARA","wincrypt/PCTL_FIND_SUBJECT_PARA"]
old-location: security\ctl_find_subject_para.htm
tech.root: security
ms.assetid: b3a63010-9025-4a86-aa48-bfb6e800a07a
ms.date: 12/05/2018
ms.keywords: '*PCTL_FIND_SUBJECT_PARA, CTL_FIND_SUBJECT_PARA, CTL_FIND_SUBJECT_PARA structure [Security], PCTL_FIND_SUBJECT_PARA, PCTL_FIND_SUBJECT_PARA structure pointer [Security], _crypto2_ctl_find_subject_para, security.ctl_find_subject_para, wincrypt/CTL_FIND_SUBJECT_PARA, wincrypt/PCTL_FIND_SUBJECT_PARA'
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
req.typenames: CTL_FIND_SUBJECT_PARA, *PCTL_FIND_SUBJECT_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CTL_FIND_SUBJECT_PARA
 - wincrypt/_CTL_FIND_SUBJECT_PARA
 - PCTL_FIND_SUBJECT_PARA
 - wincrypt/PCTL_FIND_SUBJECT_PARA
 - CTL_FIND_SUBJECT_PARA
 - wincrypt/CTL_FIND_SUBJECT_PARA
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
 - CTL_FIND_SUBJECT_PARA
---

# CTL_FIND_SUBJECT_PARA structure


## -description

The <b>CTL_FIND_SUBJECT_PARA</b> structure contains data used by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindctlinstore">CertFindCTLInStore</a> with a <i>dwFindType</i> parameter of CTL_FIND_SUBJECT to find a <a href="/windows/desktop/SecGloss/c-gly">Certificate Trust List</a> (CTL).

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field pUsagePara

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_usage_para">CTL_FIND_USAGE_PARA</a> structure. Can be <b>NULL</b> if there is no need to reference the <b>CTL_FIND_USAGE_PARA</b> parameters when finding a CTL.

### -field dwSubjectType

For CTL_CERT_SUBJECT_TYPE, the <b>pvSubject</b> member points to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>. The CTL's <b>SubjectAlgorithm</b> is examined to determine the representation of the subject's identity. Initially, only SHA1 or MD5 hash will be supported. The appropriate hash property is obtained from the <b>CERT_CONTEXT</b>. 




For CTL_ANY_SUBJECT_TYPE, <b>pvSubject</b> points to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_any_subject_info">CTL_ANY_SUBJECT_INFO</a> structure that contains the <b>SubjectAlgorithm</b> to be matched in the CTL and the <b>SubjectIdentifier</b> to be matched in one of the CTL entries.

### -field pvSubject

The value of the <b>pvSubject</b> member depends upon the value of the <b>dwSubjectType</b> member. For more information, see <b>dwSubjectType</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_any_subject_info">CTL_ANY_SUBJECT_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_usage_para">CTL_FIND_USAGE_PARA</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindctlinstore">CertFindCTLInStore</a>