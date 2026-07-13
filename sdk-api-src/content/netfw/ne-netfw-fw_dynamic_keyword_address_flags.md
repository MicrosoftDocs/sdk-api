---
UID: NE:netfw._tag_FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS
title: FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS
description: Defines constants that specify how IP addresses are to be resolved.
tech.root: ics
ms.date: 05/13/2021
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
req.typenames: FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS
req.redist: 
f1_keywords:
 - _tag_FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS
 - netfw/_tag_FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS
 - FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS
 - netfw/FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS
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
 - _tag_FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS
 - FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS
---

## -description

Defines constants that specify how IP addresses are to be resolved. See the *flags* field of [FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0).

For more info, and code examples, see [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords).

## -enum-fields

### -field FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE:0x0001

Specifies that the IP addresses will be auto-resolved and populated by another component outside the firewall service.

## -remarks

## -see-also

* [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords)
* [FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)
