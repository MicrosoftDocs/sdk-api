---
UID: NC:netfw.PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0
title: PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0
description: Function pointer type of the entry point in the service that you call to free dynamic keyword address data structs allocated by the service.
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
req.typenames: PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0
req.redist: 
f1_keywords:
 - PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0
 - netfw/PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0
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
 - PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0
---

## -description

Function pointer type of the entry point in the service that you call to free dynamic keyword address data structs allocated by the service.

> [!NOTE]
> A pointer type for this free function is published via `NetFw.h`, but a static-link library isn't published. Use the [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)/[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pattern for calling this function.

When you call [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), pass a handle to the *firewallapi.dll* module, and pass *FWFreeDynamicKeywordAddressData0* as the *lpProcName* argument.

For more info, and code examples, see [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords).

## -parameters

### -param dynamicKeywordAddressData

Type: \_In\_ **[PFW_DYNAMIC_KEYWORD_ADDRESS0](ns-netfw-fw_dynamic_keyword_address0.md)**

A pointer to either a single dynamic keyword address data object to be freed, or the head of a list of dynamic keyword address data object to be freed.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

If the function succeeds, then it returns **ERROR_SUCCESS**.

## -remarks

You should call this function only on values returned by [FWEnumDynamicKeywordAddressById0](nc-netfw-pfn_fwenumdynamickeywordaddressbyid0.md) or [FWEnumDynamicKeywordAddressesByType0](nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0.md).

## -see-also

* [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords)
