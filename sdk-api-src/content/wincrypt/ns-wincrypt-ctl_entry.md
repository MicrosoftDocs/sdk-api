---
UID: NS:wincrypt._CTL_ENTRY
title: CTL_ENTRY (wincrypt.h)
description: An element of a certificate trust list (CTL).
helpviewer_keywords: ["*PCTL_ENTRY","CTL_ENTRY","CTL_ENTRY structure [Security]","PCTL_ENTRY","PCTL_ENTRY structure pointer [Security]","_crypto2_ctl_entry","security.ctl_entry","wincrypt/CTL_ENTRY","wincrypt/PCTL_ENTRY"]
old-location: security\ctl_entry.htm
tech.root: security
ms.assetid: ebc63847-b641-4205-b15c-7b32c1426c21
ms.date: 12/05/2018
ms.keywords: '*PCTL_ENTRY, CTL_ENTRY, CTL_ENTRY structure [Security], PCTL_ENTRY, PCTL_ENTRY structure pointer [Security], _crypto2_ctl_entry, security.ctl_entry, wincrypt/CTL_ENTRY, wincrypt/PCTL_ENTRY'
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
req.typenames: CTL_ENTRY, *PCTL_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CTL_ENTRY
 - wincrypt/_CTL_ENTRY
 - PCTL_ENTRY
 - wincrypt/PCTL_ENTRY
 - CTL_ENTRY
 - wincrypt/CTL_ENTRY
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
 - CTL_ENTRY
---

# CTL_ENTRY structure


## -description

The <b>CTL_ENTRY</b> structure is an element of a <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL).

## -struct-fields

### -field SubjectIdentifier

<a href="/windows/desktop/SecGloss/b-gly">BLOB</a> containing a unique identifier of a subject. It can be a <a href="/windows/desktop/SecGloss/h-gly">hash</a> or any unique byte sequence.

### -field cAttribute

Count of elements in the <b>rgAttribute</b> member array.

### -field rgAttribute

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> structures, each holding information about the subject.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_info">CTL_INFO</a>