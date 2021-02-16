---
UID: NS:wincrypt._CTL_FIND_USAGE_PARA
title: CTL_FIND_USAGE_PARA (wincrypt.h)
description: A member of the CTL_FIND_SUBJECT_PARA structure and it is used by CertFindCTLInStore.
helpviewer_keywords: ["*PCTL_FIND_USAGE_PARA","CTL_FIND_USAGE_PARA","CTL_FIND_USAGE_PARA structure [Security]","PCTL_FIND_USAGE_PARA","PCTL_FIND_USAGE_PARA structure pointer [Security]","_crypto2_ctl_find_usage_para","security.ctl_find_usage_para","wincrypt/CTL_FIND_USAGE_PARA","wincrypt/PCTL_FIND_USAGE_PARA"]
old-location: security\ctl_find_usage_para.htm
tech.root: security
ms.assetid: bb6a7013-19ec-4263-b7a2-33c79c2b5feb
ms.date: 12/05/2018
ms.keywords: '*PCTL_FIND_USAGE_PARA, CTL_FIND_USAGE_PARA, CTL_FIND_USAGE_PARA structure [Security], PCTL_FIND_USAGE_PARA, PCTL_FIND_USAGE_PARA structure pointer [Security], _crypto2_ctl_find_usage_para, security.ctl_find_usage_para, wincrypt/CTL_FIND_USAGE_PARA, wincrypt/PCTL_FIND_USAGE_PARA'
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
req.typenames: CTL_FIND_USAGE_PARA, *PCTL_FIND_USAGE_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CTL_FIND_USAGE_PARA
 - wincrypt/_CTL_FIND_USAGE_PARA
 - PCTL_FIND_USAGE_PARA
 - wincrypt/PCTL_FIND_USAGE_PARA
 - CTL_FIND_USAGE_PARA
 - wincrypt/CTL_FIND_USAGE_PARA
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
 - CTL_FIND_USAGE_PARA
---

# CTL_FIND_USAGE_PARA structure


## -description

The <b>CTL_FIND_USAGE_PARA</b> structure is a member of the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_subject_para">CTL_FIND_SUBJECT_PARA</a> structure and it is used by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindctlinstore">CertFindCTLInStore</a>.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field SubjectUsage

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a> structure that includes a sequence of object identifiers to be matched when finding a <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL). 




A found CTL must contain all the usage object identifiers specified by the <b>SubjectUsage</b> member.

If the <b>cUsageIdentifier</b> member of this structure is zero, a CTL with any usage can be a match.

### -field ListIdentifier

Specified to restrict a search to a particular signer CTL list. Normally the <b>ListIdentifier</b> member will be zero, indicating that any <b>ListIdentifier</b> can be matched. If it is not zero, this <b>ListIdentifier</b> and the <b>ListIdentifier</b> in a CTL must match. 




To match only CTLs that have no <b>ListIdentifier</b> the <b>cbData</b> member of <b>ListIdentifier</b> is set to CTL_FIND_NO_LIST_ID_CBDATA.

A CTL uses a <b>ListIdentifier</b> to distinguish among multiple CTLs created by the same issuer with the same <b>SubjectUsage</b>.

### -field pSigner

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure that specifies the CTL signer to be matched. Only the issuer and serial number from the <b>CERT_INFO</b> are used to match a signer. 




Set <b>pSigner</b> to <b>NULL</b> to match any signer. To match CTLs that do not have any signers, set <b>pSigner</b> to CTL_FIND_NO_SIGNER_PTR.

The CertEncodingType of the signer is obtained from the <i>dwMsgAndCertEncodingType</i> parameter of 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindctlinstore">CertFindCTLInStore</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_find_subject_para">CTL_FIND_SUBJECT_PARA</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindctlinstore">CertFindCTLInStore</a>