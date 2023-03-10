---
UID: NS:winnt._LUID_AND_ATTRIBUTES
title: LUID_AND_ATTRIBUTES (winnt.h)
description: Represents a locally unique identifier (LUID) and its attributes.
helpviewer_keywords: ["*PLUID_AND_ATTRIBUTES","LUID_AND_ATTRIBUTES","LUID_AND_ATTRIBUTES structure [Security]","PLUID_AND_ATTRIBUTES","PLUID_AND_ATTRIBUTES structure pointer [Security]","_LUID_AND_ATTRIBUTES","_win32_luid_and_attributes_str","security.luid_and_attributes","winnt/LUID_AND_ATTRIBUTES","winnt/PLUID_AND_ATTRIBUTES"]
old-location: security\luid_and_attributes.htm
tech.root: security
ms.assetid: f337b561-4b67-42a0-b8de-06f546bafb26
ms.date: 12/05/2018
ms.keywords: '*PLUID_AND_ATTRIBUTES, LUID_AND_ATTRIBUTES, LUID_AND_ATTRIBUTES structure [Security], PLUID_AND_ATTRIBUTES, PLUID_AND_ATTRIBUTES structure pointer [Security], _LUID_AND_ATTRIBUTES, _win32_luid_and_attributes_str, security.luid_and_attributes, winnt/LUID_AND_ATTRIBUTES, winnt/PLUID_AND_ATTRIBUTES'
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: LUID_AND_ATTRIBUTES, *PLUID_AND_ATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LUID_AND_ATTRIBUTES
 - winnt/_LUID_AND_ATTRIBUTES
 - PLUID_AND_ATTRIBUTES
 - winnt/PLUID_AND_ATTRIBUTES
 - LUID_AND_ATTRIBUTES
 - winnt/LUID_AND_ATTRIBUTES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - LUID_AND_ATTRIBUTES
---

# LUID_AND_ATTRIBUTES structure


## -description

The <b>LUID_AND_ATTRIBUTES</b> structure represents a <a href="/windows/desktop/SecGloss/l-gly">locally unique identifier</a> (LUID) and its attributes.

## -struct-fields

### -field Luid

Specifies an <a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> value.

### -field Attributes

Specifies attributes of the LUID. This value contains up to 32 one-bit flags. Its meaning is dependent on the definition and use of the LUID.

## -remarks

An <b>LUID_AND_ATTRIBUTES</b> structure can represent an LUID whose attributes change frequently, such as when the LUID is used to represent privileges in the <a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a> structure. Privileges are represented by LUIDs and have attributes indicating whether they are currently enabled or disabled.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-allocatelocallyuniqueid">AllocateLocallyUniqueId</a>



<a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-privilege_set">PRIVILEGE_SET</a>



<a href="/windows/desktop/api/winnt/ns-winnt-token_privileges">TOKEN_PRIVILEGES</a>