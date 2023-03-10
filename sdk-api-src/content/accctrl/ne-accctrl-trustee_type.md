---
UID: NE:accctrl._TRUSTEE_TYPE
title: TRUSTEE_TYPE (accctrl.h)
description: Values that indicate the type of trustee identified by a TRUSTEE structure.
helpviewer_keywords: ["TRUSTEE_IS_ALIAS","TRUSTEE_IS_COMPUTER","TRUSTEE_IS_DELETED","TRUSTEE_IS_DOMAIN","TRUSTEE_IS_GROUP","TRUSTEE_IS_INVALID","TRUSTEE_IS_UNKNOWN","TRUSTEE_IS_USER","TRUSTEE_IS_WELL_KNOWN_GROUP","TRUSTEE_TYPE","TRUSTEE_TYPE enumeration [Security]","_win32_trustee_type_str","accctrl/TRUSTEE_IS_ALIAS","accctrl/TRUSTEE_IS_COMPUTER","accctrl/TRUSTEE_IS_DELETED","accctrl/TRUSTEE_IS_DOMAIN","accctrl/TRUSTEE_IS_GROUP","accctrl/TRUSTEE_IS_INVALID","accctrl/TRUSTEE_IS_UNKNOWN","accctrl/TRUSTEE_IS_USER","accctrl/TRUSTEE_IS_WELL_KNOWN_GROUP","accctrl/TRUSTEE_TYPE","security.trustee_type"]
old-location: security\trustee_type.htm
tech.root: security
ms.assetid: 6519c79d-9cee-4565-a71e-0b81a27c1185
ms.date: 12/05/2018
ms.keywords: TRUSTEE_IS_ALIAS, TRUSTEE_IS_COMPUTER, TRUSTEE_IS_DELETED, TRUSTEE_IS_DOMAIN, TRUSTEE_IS_GROUP, TRUSTEE_IS_INVALID, TRUSTEE_IS_UNKNOWN, TRUSTEE_IS_USER, TRUSTEE_IS_WELL_KNOWN_GROUP, TRUSTEE_TYPE, TRUSTEE_TYPE enumeration [Security], _win32_trustee_type_str, accctrl/TRUSTEE_IS_ALIAS, accctrl/TRUSTEE_IS_COMPUTER, accctrl/TRUSTEE_IS_DELETED, accctrl/TRUSTEE_IS_DOMAIN, accctrl/TRUSTEE_IS_GROUP, accctrl/TRUSTEE_IS_INVALID, accctrl/TRUSTEE_IS_UNKNOWN, accctrl/TRUSTEE_IS_USER, accctrl/TRUSTEE_IS_WELL_KNOWN_GROUP, accctrl/TRUSTEE_TYPE, security.trustee_type
req.header: accctrl.h
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
req.typenames: TRUSTEE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRUSTEE_TYPE
 - accctrl/_TRUSTEE_TYPE
 - TRUSTEE_TYPE
 - accctrl/TRUSTEE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - TRUSTEE_TYPE
---

# TRUSTEE_TYPE enumeration


## -description

The <b>TRUSTEE_TYPE</b> enumeration contains values that indicate the type of trustee identified by a 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure.

## -enum-fields

### -field TRUSTEE_IS_UNKNOWN

The trustee type is unknown, but it may be valid.

### -field TRUSTEE_IS_USER

Indicates a user.

### -field TRUSTEE_IS_GROUP

Indicates a group.

### -field TRUSTEE_IS_DOMAIN

Indicates a domain.

### -field TRUSTEE_IS_ALIAS

Indicates an alias.

### -field TRUSTEE_IS_WELL_KNOWN_GROUP

Indicates a 
<a href="/windows/desktop/SecAuthZ/well-known-sids">well-known group</a>.

### -field TRUSTEE_IS_DELETED

Indicates a deleted account.

### -field TRUSTEE_IS_INVALID

Indicates a trustee type that is not valid.

### -field TRUSTEE_IS_COMPUTER

Indicates a computer.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-enumerations">Authorization Enumerations</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>