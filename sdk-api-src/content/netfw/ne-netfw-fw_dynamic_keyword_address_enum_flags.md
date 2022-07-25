---
UID: NE:netfw._tag_FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS
title: FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS
description: Defines constants that specify the kind(s) of objects to include in an enumeration operation.
tech.root: ics
ms.date: 05/14/2021
req.construct-type: enumeration
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.typenames: FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS
req.redist: 
f1_keywords:
 - _tag_FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS
 - netfw/_tag_FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS
 - FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS
 - netfw/FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - firewallapi.dll
api_name:
 - _tag_FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS
 - FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS
---

## -description

Defines constants that specify the kind(s) of objects to include in an enumeration operation.

For more info, and code examples, see [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords).

## -enum-fields

### -field FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_AUTO_RESOLVE:0x0001

Specifies that enumeration should include all objects that have the [FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE](ne-netfw-fw_dynamic_keyword_address_flags.md) flag set.

### -field FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_NON_AUTO_RESOLVE:0x0002

Specifies that enumeration should include all objects that have the [FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE](ne-netfw-fw_dynamic_keyword_address_flags.md) flag *not* set.

### -field FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_ALL

Specifies that enumeration should include *all* objects.

## -remarks

## -see-also

* [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords)
