---
UID: NF:fwpmu.FwpmDynamicKeywordSubscribe0
title: FwpmDynamicKeywordSubscribe0
description: Requests the delivery of notifications regarding changes to particular dynamic keyword address ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) objects.
tech.root: fwp
ms.date: 05/17/2021
req.construct-type: function
req.header: fwpmu.h
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
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - FwpmDynamicKeywordSubscribe0
 - fwpmu/FwpmDynamicKeywordSubscribe0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmDynamicKeywordSubscribe0
---

## -description

Requests the delivery of notifications regarding changes to particular dynamic keyword address ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) objects. Based on the flag passed in, notifications can be raised for only a subset of the addresses.

For more info, and code examples, see [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords).

## -parameters

### -param flags

Type: \_In\_ **[DWORD](/windows/win32/winprog/windows-data-types)**

The following flags are defined in `fwpmu.h`.

**FWPM_NOTIFY_ADDRESSES_AUTO_RESOLVE** indicates that notifications will be delivered only for objects that have the [FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE](/windows/win32/api/netfw/ne-netfw-fw_dynamic_keyword_address_flags) flag set.

**FWPM_NOTIFY_ADDRESSES_NON_AUTO_RESOLVE** indicates that notifications will be delivered only for objects that *don't* have the [FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE](/windows/win32/api/netfw/ne-netfw-fw_dynamic_keyword_address_flags) flag set.

**FWPM_NOTIFY_ADDRESSES_AUTO_RESOLVE** indicates that notifications will be delivered for *all* dynamic keyword address objects.

### -param callback

Type: \_In\_ **[FWPM_DYNAMIC_KEYWORD_CALLBACK0](nc-fwpmu-fwpm_dynamic_keyword_callback0.md)**

A pointer to a callback function that you implement, which will be invoked when a notification is ready for delivery.

### -param context

Type: \_In\_opt\_ **void\***

An optional context pointer. This pointer is passed to the callback function.

### -param subscriptionHandle

Type: \_Out\_ **[HANDLE](/windows/win32/winprog/windows-data-types)\***

The address of a handle, which is populated with a handle to the newly created subscription.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

If the function succeeds, then it returns **ERROR_SUCCESS**. Otherwise, it returns one of the following values.

|Return value|Description|
|-|-|
|ERROR_INVALID_PARAMETER|The *flags* value is zero.|

## -remarks

Notifications for *AutoResolve* dynamic keyword addresses are delivered when an object is added or deleted.

Notifications for *non-AutoResolve* dynamic keyword addresses are delivered when an object is added, deleted, or updated.

No data is provided to the callback function. You can use the **Enumeration** API if you need information about what has changed on the system.

You're responsible for closing the handle when you no longer need subscription. You must do so by calling the [FwpmDynamicKeywordUnsubscribe0](nf-fwpmu-fwpmdynamickeywordunsubscribe0.md) function.

Your implementation of [FWPM_DYNAMIC_KEYWORD_CALLBACK0](nc-fwpmu-fwpm_dynamic_keyword_callback0.md) should react to changes in dynamic keyword address objects quickly, because it is scheduled on a ThreadPool thread, and could affect other wait operations.

## -see-also

* [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords)
* [FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)
* [FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS](/windows/win32/api/netfw/ne-netfw-fw_dynamic_keyword_address_flags)
