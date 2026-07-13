---
UID: NC:netfw.PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0
title: PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0
description: Function pointer type of the entry point in the service that you call to enumerate dynamic keyword addresses by type. You can request a particular subset of objects based on the enumeration flags passed in.
tech.root: ics
ms.date: 05/14/2021
req.construct-type: function
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
req.dll: firewallapi.dll
req.irql: 
targetos: Windows
req.typenames: PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0
req.redist: 
f1_keywords:
 - PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0
 - netfw/PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - UserDefined
api_location:
 - netfw.h
 - firewallapi.dll
api_name:
 - PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0
---

## -description

Function pointer type of the entry point in the service that you call to enumerate dynamic keyword addresses by type. You can request a particular subset of objects based on the enumeration flags passed in.

> [!NOTE]
> A pointer type for this free function is published via `NetFw.h`, but a static-link library isn't published. Use the [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)/[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pattern for calling this function.

When you call [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), pass a handle to the *firewallapi.dll* module, and pass *FWEnumDynamicKeywordAddressesByType0* as the *lpProcName* argument.

For more info, and code examples, see [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords).

## -parameters

### -param flags

Type: **[DWORD](/windows/win32/api/guiddef/ns-guiddef-guid)**

Using the value [FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_AUTO_RESOLVE](ne-netfw-fw_dynamic_keyword_address_enum_flags.md) will enumerate all objects that have the [FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE](ne-netfw-fw_dynamic_keyword_address_flags.md) flag set.

Using the value [FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_NON_AUTO_RESOLVE](ne-netfw-fw_dynamic_keyword_address_enum_flags.md) will enumerate all objects that have the [FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE](ne-netfw-fw_dynamic_keyword_address_flags.md) flag *not* set.

Using the value [FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_NON_AUTO_RESOLVE](ne-netfw-fw_dynamic_keyword_address_enum_flags.md) will enumerate *all* objects.

### -param dynamicKeywordAddressData

Type: \_Out\_ **[PFW_DYNAMIC_KEYWORD_ADDRESS0](ns-netfw-fw_dynamic_keyword_address0.md)\***

The address of a pointer to a dynamic keyword address object, which will hold a linked list of objects returned. You must free this address by calling [FWFreeDynamicKeywordAddressData0](nc-netfw-pfn_fwfreedynamickeywordaddressdata0.md).

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

If the function succeeds, then it returns **ERROR_SUCCESS**. Otherwise, it returns one of the following values.

|Return value|Description|
|-|-|
|ERROR_INVALID_PARAMETER|A zero value was passed in for the *flags* parameter.|

## -remarks

You must free the address of the first returned object in the list (the head of the list) by calling [FWFreeDynamicKeywordAddressData0](nc-netfw-pfn_fwfreedynamickeywordaddressdata0.md).

## -see-also

* [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords)
