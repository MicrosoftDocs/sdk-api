---
UID: NS:subauth._UNICODE_STRING
title: "_UNICODE_STRING"
author: windows-driver-content
description: Used by various Local Security Authority (LSA) functions to specify a Unicode string.
old-location: security\unicode_string.htm
old-project: SecAuthN
ms.assetid: 4687d63a-4e58-4181-a48f-2724e5015e77
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PUNICODE_STRING, LSA_UNICODE_STRING, LSA_UNICODE_STRING structure [Security], PLSA_UNICODE_STRING, PLSA_UNICODE_STRING structure pointer [Security], PUNICODE_STRING, PUNICODE_STRING structure pointer [Security], UNICODE_STRING, UNICODE_STRING structure [Security], _UNICODE_STRING, _lsa_unicode_string, ntsecapi/PLSA_UNICODE_STRING, ntsecapi/PUNICODE_STRING, ntsecapi/UNICODE_STRING, security.unicode_string, subauth/PLSA_UNICODE_STRING, subauth/PUNICODE_STRING, subauth/UNICODE_STRING"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: UNICODE_STRING, *PUNICODE_STRING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Subauth.h
-	Ntsecapi.h
api_name:
-	LSA_UNICODE_STRING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _UNICODE_STRING structure


## -description


The <b>UNICODE_STRING</b> structure is used by various <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) functions to specify a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> string.


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

