---
UID: NC:netfw.PFN_FWDELETEDYNAMICKEYWORDADDRESS0
title: PFN_FWDELETEDYNAMICKEYWORDADDRESS0
description: Function pointer type of the entry point in the service that you call to delete the dynamic keyword address with the specified ID.
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
req.typenames: PFN_FWDELETEDYNAMICKEYWORDADDRESS0
req.redist: 
f1_keywords:
 - PFN_FWDELETEDYNAMICKEYWORDADDRESS0
 - netfw/PFN_FWDELETEDYNAMICKEYWORDADDRESS0
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
 - PFN_FWDELETEDYNAMICKEYWORDADDRESS0
---

## -description

Function pointer type of the entry point in the service that you call to delete the dynamic keyword address with the specified ID.

> [!NOTE]
> A pointer type for this free function is published via `NetFw.h`, but a static-link library isn't published. Use the [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)/[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pattern for calling this function.

When you call [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), pass a handle to the *firewallapi.dll* module, and pass *FWDeleteDynamicKeywordAddress0* as the *lpProcName* argument.

For more info, and code examples, see [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords).

## -parameters

### -param dynamicKeywordAddressId

Type: **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)**

The id of the dynamic keyword address object to delete.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

If the function succeeds (the object was successfully deleted, or no object with the specified ID exists), then it returns **ERROR_SUCCESS**. Otherwise, it returns one of the following values.

|Return value|Description|
|-|-|
|ERROR_ACCESS_DENIED|The caller doesn't have proper permissions to operate on the object with the specified ID. This likely means that the object is managed by MDM (it has origin type **FW_DYNAMIC_KEYWORD_ORIGIN_MDM**.|

## -remarks

> [!NOTE]
> This function returns **ERROR_SUCCESS** even if the object with the specified ID doesn't exist.

## -see-also

* [Firewall dynamic keywords](/windows/win32/ics/firewall-dynamic-keywords)
