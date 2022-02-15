---
UID: NS:netfw._tag_FW_DYNAMIC_KEYWORD_ADDRESS_DATA0
title: FW_DYNAMIC_KEYWORD_ADDRESS_DATA0
description: Holds the data returned to the client when the **Enumeration** APIs are called.
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
req.typenames: FW_DYNAMIC_KEYWORD_ADDRESS_DATA0, *PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0
req.redist: 
f1_keywords:
 - _tag_FW_DYNAMIC_KEYWORD_ADDRESS_DATA0
 - netfw/_tag_FW_DYNAMIC_KEYWORD_ADDRESS_DATA0
 - PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0
 - netfw/PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0
 - FW_DYNAMIC_KEYWORD_ADDRESS_DATA0
 - netfw/FW_DYNAMIC_KEYWORD_ADDRESS_DATA0
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - firewallapi.dll
api_name:
 - _tag_FW_DYNAMIC_KEYWORD_ADDRESS_DATA0
 - PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0
 - FW_DYNAMIC_KEYWORD_ADDRESS_DATA0
---

## -description

Holds the data returned to the client when the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) or [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) APIs are called. This structure holds the dynamic keyword address object, as well as additional metadata.

For more info, and code examples, see [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords).

## -struct-fields

### -field dynamicKeywordAddress

Type: **[FW_DYNAMIC_KEYWORD_ADDRESS0](ns-netfw-fw_dynamic_keyword_address0.md)**

A dynamic keyword address (the dynamic keyword address object).

### -field next

Type: **[FW_DYNAMIC_KEYWORD_ADDRESS0](ns-netfw-fw_dynamic_keyword_address0.md)\***

A pointer to the next dynamic keyword address object in a linked list.

### -field schemaVersion

Type: **[WORD](/windows/win32/api/guiddef/ns-guiddef-guid)**

The schema version of the object. This is used by the [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) API.

### -field originType

Type: **[FW_DYNAMIC_KEYWORD_ORIGIN_TYPE](ne-netfw-fw_dynamic_keyword_origin_type.md)**

Indicates the origin of this object. It can be either **FW_DYNAMIC_KEYWORD_ORIGIN_LOCAL**, which represents a locally created object, or **FW_DYNAMIC_KEYWORD_ORIGIN_MDM**, which represents an MDM managed object.

## -remarks

## -see-also

* [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords)
* [FWEnumDynamicKeywordAddressById0](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0)
* [FWEnumDynamicKeywordAddressesByType0](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0)
* [FWFreeDynamicKeywordAddressData0](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0)
