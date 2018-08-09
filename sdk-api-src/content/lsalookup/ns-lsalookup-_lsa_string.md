---
UID: NS:lsalookup._LSA_STRING
title: "_LSA_STRING"
author: windows-sdk-content
description: Used by Local Security Authority (LSA) functions to specify an ANSI string.
old-location: security\lsa_string.htm
old-project: secauthn
ms.assetid: 4ae4160f-bcad-41d9-8239-91da44702b76
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PLSA_STRING, LSA_STRING, LSA_STRING structure [Security], PLSA_STRING, PLSA_STRING structure pointer [Security], _LSA_STRING, _lsa_lsa_string, lsalookup/LSA_STRING, lsalookup/PLSA_STRING, security.lsa_string"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: LSA_STRING, *PLSA_STRING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - LsaLookup.h
api_name:
 - LSA_STRING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _LSA_STRING structure


## -description


The <b>LSA_STRING</b> structure is used by <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) functions to specify an ANSI string.


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

