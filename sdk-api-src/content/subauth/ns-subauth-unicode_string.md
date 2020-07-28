---
UID: NS:subauth._UNICODE_STRING
title: UNICODE_STRING (subauth.h)
description: Used by various Local Security Authority (LSA) functions to specify a Unicode string.
helpviewer_keywords: ["*PUNICODE_STRING","LSA_UNICODE_STRING","LSA_UNICODE_STRING structure [Security]","PLSA_UNICODE_STRING","PLSA_UNICODE_STRING structure pointer [Security]","PUNICODE_STRING","PUNICODE_STRING structure pointer [Security]","UNICODE_STRING","UNICODE_STRING structure [Security]","_lsa_unicode_string","ntsecapi/PLSA_UNICODE_STRING","ntsecapi/PUNICODE_STRING","ntsecapi/UNICODE_STRING","security.unicode_string","subauth/PLSA_UNICODE_STRING","subauth/PUNICODE_STRING","subauth/UNICODE_STRING"]
old-location: security\unicode_string.htm
tech.root: security
ms.assetid: 4687d63a-4e58-4181-a48f-2724e5015e77
ms.date: 12/05/2018
ms.keywords: '*PUNICODE_STRING, LSA_UNICODE_STRING, LSA_UNICODE_STRING structure [Security], PLSA_UNICODE_STRING, PLSA_UNICODE_STRING structure pointer [Security], PUNICODE_STRING, PUNICODE_STRING structure pointer [Security], UNICODE_STRING, UNICODE_STRING structure [Security], _lsa_unicode_string, ntsecapi/PLSA_UNICODE_STRING, ntsecapi/PUNICODE_STRING, ntsecapi/UNICODE_STRING, security.unicode_string, subauth/PLSA_UNICODE_STRING, subauth/PUNICODE_STRING, subauth/UNICODE_STRING'
f1_keywords:
- subauth/LSA_UNICODE_STRING
dev_langs:
- c++
req.header: subauth.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Subauth.h
- Ntsecapi.h
api_name:
- LSA_UNICODE_STRING
targetos: Windows
req.typenames: UNICODE_STRING, *PUNICODE_STRING
req.redist: 
ms.custom: 19H1
---

# UNICODE_STRING structure


## -description


The <b>UNICODE_STRING</b> structure is used by various <a href="https://docs.microsoft.com/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA) functions to specify a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/u-gly">Unicode</a> string.


## -struct-fields




### -field Length

Specifies the length, in bytes, of the string pointed to by the <b>Buffer</b> member, not including the terminating <b>NULL</b> character, if any.

<b>Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>When the <b>Length</b> structure member is zero and the <b>MaximumLength</b> structure member is 1, the <b>Buffer</b> structure member can be an empty string or contain solely a null character. This behavior changed beginning with Windows Server 2008 R2 and Windows 7 with SP1.


### -field MaximumLength

Specifies the total size, in bytes, of memory allocated for <b>Buffer</b>. Up to <b>MaximumLength</b> bytes may be written into the buffer without trampling memory.

<b>Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>When the <b>Length</b> structure member is zero and the <b>MaximumLength</b> structure member is 1, the <b>Buffer</b> structure member can be an empty string or contain solely a null character. This behavior changed beginning with Windows Server 2008 R2 and Windows 7 with SP1.


### -field Buffer

Pointer to a wide-character string. Note that the strings returned by the various LSA functions might not be <b>null</b>-terminated.

<b>Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>When the <b>Length</b> structure member is zero and the <b>MaximumLength</b> structure member is 1, the <b>Buffer</b> structure member can be an empty string or contain solely a null character. This behavior changed beginning with Windows Server 2008 R2 and Windows 7 with SP1.

