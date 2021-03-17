---
UID: NS:lsalookup._LSA_STRING
title: LSA_STRING (lsalookup.h)
description: Used by Local Security Authority (LSA) functions to specify an ANSI string.
helpviewer_keywords: ["*PLSA_STRING","LSA_STRING","LSA_STRING structure [Security]","PLSA_STRING","PLSA_STRING structure pointer [Security]","_lsa_lsa_string","lsalookup/LSA_STRING","lsalookup/PLSA_STRING","security.lsa_string"]
old-location: security\lsa_string.htm
tech.root: security
ms.assetid: 4ae4160f-bcad-41d9-8239-91da44702b76
ms.date: 12/05/2018
ms.keywords: '*PLSA_STRING, LSA_STRING, LSA_STRING structure [Security], PLSA_STRING, PLSA_STRING structure pointer [Security], _lsa_lsa_string, lsalookup/LSA_STRING, lsalookup/PLSA_STRING, security.lsa_string'
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
req.typenames: LSA_STRING, *PLSA_STRING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LSA_STRING
 - lsalookup/_LSA_STRING
 - PLSA_STRING
 - lsalookup/PLSA_STRING
 - LSA_STRING
 - lsalookup/LSA_STRING
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
 - LSA_STRING
---

# LSA_STRING structure


## -description

The <b>LSA_STRING</b> structure is used by <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) functions to specify an ANSI string.

## -struct-fields

### -field Length

Specifies the length, in bytes, of the string in <b>Buffer</b>. This value does not include the terminating null character, if any.

When the <b>Length</b> structure member is zero and the <b>MaximumLength</b> structure member is 1, the <b>Buffer</b> structure member must not be an empty string or contain solely a null character.

<b>Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>When the <b>Length</b> structure member is zero and the <b>MaximumLength</b> structure member is 1, the <b>Buffer</b> structure member can be an empty string or contain solely a null character. This behavior changed beginning with Windows Server 2008 R2 and Windows 7 with SP1.

### -field MaximumLength

Specifies the total size, in bytes, of <b>Buffer</b>. Up to <b>MaximumLength</b> bytes may be written into the buffer without trampling memory.

When the <b>Length</b> structure member is zero and the <b>MaximumLength</b> structure member is 1, the <b>Buffer</b> structure member must not be an empty string or contain solely a null character.

<b>Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>When the <b>Length</b> structure member is zero and the <b>MaximumLength</b> structure member is 1, the <b>Buffer</b> structure member can be an empty string or contain solely a null character. This behavior changed beginning with Windows Server 2008 R2 and Windows 7 with SP1.

### -field Buffer

Pointer to an array of characters. Note that strings returned by the LSA may not be null-terminated.

When the <b>Length</b> structure member is zero and the <b>MaximumLength</b> structure member is 1, the <b>Buffer</b> structure member must not be an empty string or contain solely a null character.

<b>Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>When the <b>Length</b> structure member is zero and the <b>MaximumLength</b> structure member is 1, the <b>Buffer</b> structure member can be an empty string or contain solely a null character. This behavior changed beginning with Windows Server 2008 R2 and Windows 7 with SP1.