---
UID: NC:netfw.PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0
title: PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0
description: Function pointer type of the entry point in the service that you call to enumerate the specific dynamic keyword addresses by ID.
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
req.typenames: PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0
req.redist: 
f1_keywords:
 - PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0
 - netfw/PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0
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
 - PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0
---

## -description

Function pointer type of the entry point in the service that you call to enumerate the specific dynamic keyword addresses by ID.

> [!NOTE]
> A pointer type for this free function is published via `NetFw.h`, but a static-link library isn't published. Use the [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)/[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pattern for calling this function.

When you call [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), pass a handle to the *firewallapi.dll* module, and pass *FWEnumDynamicKeywordAddressById0* as the *lpProcName* argument.

For more info, and code examples, see [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords).

## -parameters

### -param dynamicKeywordAddressId

Type: **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)**

The id of the dynamic keyword address object to enumerate.

### -param dynamicKeywordAddressData

Type: \_Out\_ **[PFW_DYNAMIC_KEYWORD_ADDRESS0](ns-netfw-fw_dynamic_keyword_address0.md)\***

The address of a pointer to a dynamic keyword address object, which will hold the object returned. You must free this object by calling [FWFreeDynamicKeywordAddressData0](nc-netfw-pfn_fwfreedynamickeywordaddressdata0.md).

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

If the function succeeds, then it returns **ERROR_SUCCESS**.

## -remarks

If the object returned via *dynamicKeywordAddressData* is non-NULL, then its *pNext* field is always null.

You must free the returned addresses object by calling [FWFreeDynamicKeywordAddressData0](nc-netfw-pfn_fwfreedynamickeywordaddressdata0.md).

## -see-also

* [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords)
