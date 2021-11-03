---
UID: NC:netfw.PFN_FWADDDYNAMICKEYWORDADDRESS0
title: PFN_FWADDDYNAMICKEYWORDADDRESS0
description: Function pointer type of the entry point in the service that you call to add the specified dynamic keyword address.
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
req.typenames: PFN_FWADDDYNAMICKEYWORDADDRESS0
req.redist: 
f1_keywords:
 - PFN_FWADDDYNAMICKEYWORDADDRESS0
 - netfw/PFN_FWADDDYNAMICKEYWORDADDRESS0
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
 - PFN_FWADDDYNAMICKEYWORDADDRESS0
---

## -description

Function pointer type of the entry point in the service that you call to add the specified dynamic keyword address.

> [!NOTE]
> A pointer type for this free function is published via `NetFw.h`, but a static-link library isn't published. Use the [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)/[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pattern for calling this function.

When you call [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), pass a handle to the *firewallapi.dll* module, and pass *FWAddDynamicKeywordAddress0* as the *lpProcName* argument.

For more info, and code examples, see [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords).

## -parameters

### -param dynamicKeywordAddress

Type: **const [PFW_DYNAMIC_KEYWORD_ADDRESS0](ns-netfw-fw_dynamic_keyword_address0.md)**

A pointer to a constant (populated) dynamic keyword address object.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

If the function succeeds (the object was successfully created and added), then it returns **ERROR_SUCCESS**. Otherwise, it returns one of the following values.

|Return value|Description|
|-|-|
|ERROR_ACCESS_DENIED|The caller doesn't have proper permissions to create this object.|
|ERROR_ALREADY_EXISTS|An object with the specified ID already exists on the system.|
|ERROR_INVALID_PARAMETER|Invalid [FW_DYNAMIC_KEYWORD_ADDRESS0](ns-netfw-fw_dynamic_keyword_address0.md). See [**Remarks**](#remarks) for valid usage.|

## -remarks

* If the **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** flag is set, then:
  * the *addresses* must be NULL, and
  * the *keyword* field should be a string that can be resolved; that is, a FQDN or hostname.
* If the **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** flag is *not* set, then the *addresses* field must be a comma-separated list of IP address tokens. Tokens can be individual IP addresses, ranges, or subnets. Valid token formats include:
  * A valid IPv4 address (for example, 10.0.0.10)
  * A valid IPv6 address (for example, 2620:1ec:c11::200)
  * An IPv4 address range in the format \<start address\>-\<end address\>, with no spaces included (for example, 10.0.0.0-10.0.0.255)
  * An IPv6 address range in the format \<start address\>-\<end address\>, with no spaces included (for example, 2001:db8:abcd:12::-2001:db8:abcd:12:ffff:ffff:ffff:ffff)
  * A valid IPv4 subnet specified using the network prefix notation (for example, 10.0.0.0/24)
  * A valid IPv6 subnet specified using the prefix length notation (for example, 2001:db8:abcd:0012::0/64)
* A dynamic keyword address persists across reboots. For the *AutoResolved* objects, the addresses are *not* persisted across boot cycles, and must be re-evaluated during the following boot cycle.

## -see-also

* [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords)
