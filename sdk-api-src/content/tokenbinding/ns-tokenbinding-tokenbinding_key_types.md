---
UID: NS:tokenbinding.TOKENBINDING_KEY_TYPES
title: TOKENBINDING_KEY_TYPES (tokenbinding.h)
description: Contains all of the combinations of types of token binding keys that a client device or server supports.
helpviewer_keywords: ["TOKENBINDING_KEY_TYPES","TOKENBINDING_KEY_TYPES structure [Security]","security.tokenbinding_key_types","tokenbinding/TOKENBINDING_KEY_TYPES"]
old-location: security\tokenbinding_key_types.htm
tech.root: security
ms.assetid: E5029CE3-CD23-4566-A951-35374DC7BC57
ms.date: 12/05/2018
ms.keywords: TOKENBINDING_KEY_TYPES, TOKENBINDING_KEY_TYPES structure [Security], security.tokenbinding_key_types, tokenbinding/TOKENBINDING_KEY_TYPES
req.header: tokenbinding.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: TOKENBINDING_KEY_TYPES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TOKENBINDING_KEY_TYPES
 - tokenbinding/TOKENBINDING_KEY_TYPES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - tokenbinding.h
api_name:
 - TOKENBINDING_KEY_TYPES
---

# TOKENBINDING_KEY_TYPES structure


## -description

Contains all of the combinations of  types of token binding keys that a client device or server supports.

## -struct-fields

### -field keyCount

The number of elements in the array that the <b>key</b> member contains.

### -field keyType

 




#### - key

An array of all of the combinations of  types of token binding keys that a client device or server supports. These keys map one-to-one to Application Layer Protocol Negotiation (ALPN) protocol identifiers. You must maintain the table of these mappings.

## -see-also

<a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindinggetkeytypesclient">TokenBindingGetKeyTypesClient</a>



<a href="/windows/desktop/api/tokenbinding/nf-tokenbinding-tokenbindinggetkeytypesserver">TokenBindingGetKeyTypesServer</a>