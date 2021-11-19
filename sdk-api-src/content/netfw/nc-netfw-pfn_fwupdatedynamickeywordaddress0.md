---
UID: NC:netfw.PFN_FWUPDATEDYNAMICKEYWORDADDRESS0
title: PFN_FWUPDATEDYNAMICKEYWORDADDRESS0
description: Function pointer type of the entry point in the service that you call to update the dynamic keyword address with the input ID.
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
req.typenames: PFN_FWUPDATEDYNAMICKEYWORDADDRESS0
req.redist: 
f1_keywords:
 - PFN_FWUPDATEDYNAMICKEYWORDADDRESS0
 - netfw/PFN_FWUPDATEDYNAMICKEYWORDADDRESS0
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
 - PFN_FWUPDATEDYNAMICKEYWORDADDRESS0
---

## -description

Function pointer type of the entry point in the service that you call to update the dynamic keyword address with the input ID.

> [!NOTE]
> A pointer type for this free function is published via `NetFw.h`, but a static-link library isn't published. Use the [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)/[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pattern for calling this function.

When you call [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), pass a handle to the *firewallapi.dll* module, and pass *FWFreeDynamicKeywordAddressData0* as the *lpProcName* argument.

For more info, and code examples, see [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords).

## -parameters

### -param dynamicKeywordAddressId

Type: **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)**

The id of the dynamic keyword address object to update.

### -param updatedAddresses

Type: **[PCWSTR](/windows/win32/winprog/windows-data-types)**

A comma-separated list of IP addresses, subnets, or ranges to update the object with.

### -param append

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

Set to **TRUE**, and the *updatedAddresses* will be appended to the object's current list of addresses. Set to **FALSE**, and the *updatedAddresses* will replace the object's current list of addresses.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

If the function succeeds (the object was successfully updated), then it returns **ERROR_SUCCESS**. Otherwise, it returns one of the following values.

|Return value|Description|
|-|-|
|ERROR_ACCESS_DENIED|The caller doesn't have proper permissions to operate on the object with the specified ID. This error occurs when this API is called on *non-AutoResolve* objects managed by MDM.|
|ERROR_INVALID_PARAMETER|Common error conditions include: No object with the specified ID exists; the addresses are in an invalid format.|

## -remarks

If *append* is **TRUE**, then the input addresses will be appended to the object's current list of addresses. If the input parameter is a duplicate of an address already set in the object, then it will be discarded, and **ERROR_SUCCESS** will be returned.

The firewall service treats an address as a duplicate if the address is exactly equivalent to a value in the dynamic keyword address's existing addresses field. Duplicate values are considered on an individual element basis, so an update with a list of IP addresses might have only a subset of duplicate input discarded. For example, if the dynamic keyword address object contains `127.0.0.0-127.0.0.255`, then any input of `127.0.0.0-127.0.0.255` or `127.0.0.0/24` would be discarded. However, an input such as `127.0.0.0-127.0.0.40` would not be discarded, since that is a subset, and not a direct duplicate.

If *append* is **FALSE**, then the object's current list of addresses will be overwritten by the input.

*Non-AutoResolve* objects that originated from MDM will result in **ERROR_ACCESS_DENIED**.

*Non-AutoResolve* objects that were locally created (through API or PowerShell) are updated via this API.

*AutoResolve* objects of any origin are updateable via this API.

To clear the addresses for an object, pass in NULL for the *updatedAddresses* value.

Valid format for the *updatedAddresses* parameter is a comma-separated list of IP address tokens. Tokens can be individual IP addresses, ranges, or subnets. Valid token formats include:
  * A valid IPv4 address (for example, 10.0.0.10)
  * A valid IPv6 address (for example, 2620:1ec:c11::200)
  * An IPv4 address range in the format \<start address\>-\<end address\>, with no spaces included (for example, 10.0.0.0-10.0.0.255)
  * An IPv6 address range in the format \<start address\>-\<end address\>, with no spaces included (for example, 2001:db8:abcd:12::-2001:db8:abcd:12:ffff:ffff:ffff:ffff)
  * A valid IPv4 subnet specified using the network prefix notation (for example, 10.0.0.0/24)
  * A valid IPv6 subnet specified using the prefix length notation (for example, 2001:db8:abcd:0012::0/64)

## -see-also

* [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords)
