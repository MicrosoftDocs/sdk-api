---
UID: NS:netfw._tag_FW_DYNAMIC_KEYWORD_ADDRESS0
title: FW_DYNAMIC_KEYWORD_ADDRESS0
description: Allows the client to create a dynamic keyword address, which holds a list of IP addresses.
tech.root: ics
ms.date: 05/13/2021
req.construct-type: structure
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
req.typenames: FW_DYNAMIC_KEYWORD_ADDRESS0, *PFW_DYNAMIC_KEYWORD_ADDRESS0
req.redist: 
f1_keywords:
 - _tag_FW_DYNAMIC_KEYWORD_ADDRESS0
 - netfw/_tag_FW_DYNAMIC_KEYWORD_ADDRESS0
 - PFW_DYNAMIC_KEYWORD_ADDRESS0
 - netfw/PFW_DYNAMIC_KEYWORD_ADDRESS0
 - FW_DYNAMIC_KEYWORD_ADDRESS0
 - netfw/FW_DYNAMIC_KEYWORD_ADDRESS0
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - firewallapi.dll
api_name:
 - _tag_FW_DYNAMIC_KEYWORD_ADDRESS0
 - PFW_DYNAMIC_KEYWORD_ADDRESS0
 - FW_DYNAMIC_KEYWORD_ADDRESS0
---

## -description

Allows the client to create a dynamic keyword address, which holds a list of IP addresses. This object can also be marked as *AutoResolve*, which indicates that the IP addresses are not populated upon creation, but instead populated by a component outside of the firewall service.

For more info, and code examples, see [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords).

## -struct-fields

### -field id

Type: **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)**

A unique **GUID** identifier for this object. It must be a non-empty **GUID**.

### -field keyword

Type: **[PCWSTR](/windows/win32/api/guiddef/ns-guiddef-guid)**

Either a string (for management convenience), or a resolvable string (that is, a FQDN or hostname) when the **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** flag is set.

### -field flags

Type: **[DWORD](/windows/win32/api/guiddef/ns-guiddef-guid)**

Set to the value [**FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE**](/windows/win32/api/netfw/ne-netfw-fw_dynamic_keyword_address_flags) to indicate that the *keyword* field will be resolved, and that the *addresses* field will be populated by another component outside the firewall service.

### -field addresses

Type: **[PCWSTR](/windows/win32/api/guiddef/ns-guiddef-guid)**

The list of IP addresses for this keyword. If the **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** flag is set, then this indicates that the *addresses* field was populated outside the firewall service.

## -remarks

## -see-also

* [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords)
