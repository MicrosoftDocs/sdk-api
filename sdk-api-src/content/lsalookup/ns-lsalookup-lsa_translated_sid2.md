---
UID: NS:lsalookup._LSA_TRANSLATED_SID2
title: LSA_TRANSLATED_SID2 (lsalookup.h)
description: Contains SIDs that are retrieved based on account names.
helpviewer_keywords: ["*PLSA_TRANSLATED_SID2","LSA_TRANSLATED_SID2","LSA_TRANSLATED_SID2 structure [Security]","PLSA_TRANSLATED_SID2","PLSA_TRANSLATED_SID2 structure pointer [Security]","_lsa_lsa_translated_sid2","lsalookup/LSA_TRANSLATED_SID2","lsalookup/PLSA_TRANSLATED_SID2","security.lsa_translated_sid2"]
old-location: security\lsa_translated_sid2.htm
tech.root: security
ms.assetid: 792de958-8e24-46d8-b484-159435bc96e3
ms.date: 12/05/2018
ms.keywords: '*PLSA_TRANSLATED_SID2, LSA_TRANSLATED_SID2, LSA_TRANSLATED_SID2 structure [Security], PLSA_TRANSLATED_SID2, PLSA_TRANSLATED_SID2 structure pointer [Security], _lsa_lsa_translated_sid2, lsalookup/LSA_TRANSLATED_SID2, lsalookup/PLSA_TRANSLATED_SID2, security.lsa_translated_sid2'
req.header: lsalookup.h
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
req.typenames: LSA_TRANSLATED_SID2, *PLSA_TRANSLATED_SID2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LSA_TRANSLATED_SID2
 - lsalookup/_LSA_TRANSLATED_SID2
 - PLSA_TRANSLATED_SID2
 - lsalookup/PLSA_TRANSLATED_SID2
 - LSA_TRANSLATED_SID2
 - lsalookup/LSA_TRANSLATED_SID2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LsaLookup.h
api_name:
 - LSA_TRANSLATED_SID2
---

# LSA_TRANSLATED_SID2 structure


## -description

The <b>LSA_TRANSLATED_SID2</b> structure contains 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SIDs</a> that are retrieved based on account names. This structure is used by the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames2">LsaLookupNames2</a> function.

## -struct-fields

### -field Use

An 
<a href="/windows/desktop/api/winnt/ne-winnt-sid_name_use">SID_NAME_USE</a> enumeration value that identifies the use of the SID. If this value is SidTypeUnknown or SidTypeInvalid, the rest of the information in the structure is not valid and should be ignored.

### -field Sid

The complete SID of the account.

### -field DomainIndex

The index of an entry in a related 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list">LSA_REFERENCED_DOMAIN_LIST</a> data structure which describes the domain that owns the account. If there is no corresponding reference domain for an entry, then <b>DomainIndex</b> will contain a negative value.

### -field Flags

Not used.