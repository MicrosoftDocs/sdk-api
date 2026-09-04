---
UID: NF:apiquery2.IsApiSetImplemented
title: IsApiSetImplemented function (apiquery2.h)
description: The IsApiSetImplemented function tests if a specified API set is present on the computer.
helpviewer_keywords: ["IsApiSetImplemented","IsApiSetImplemented function [Windows API]","apiquery2/IsApiSetImplemented","winprog.isapisetimplemented"]
old-location: winprog\isapisetimplemented.htm
tech.root: winprog
ms.assetid: DF177716-9F33-4E39-BD63-D1B8E39CD67C
ms.date: 09/03/2026
ms.keywords: IsApiSetImplemented, IsApiSetImplemented function [Windows API], apiquery2/IsApiSetImplemented, winprog.isapisetimplemented
req.construct-type: function
req.header: apiquery2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: onecore.lib
req.dll: api-ms-win-core-apiquery-l2-1-0.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsApiSetImplemented
 - apiquery2/IsApiSetImplemented
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-apiquery-l2-1-0.dll
api_name:
 - IsApiSetImplemented
---

## -description

Tests whether a specified *API set* is present on the computer.

## -parameters

### -param Contract

Specifies the name of the API set to query, without a `.dll` suffix. For more info, see the Remarks section.

## -returns

**IsApiSetImplemented** returns **TRUE** if the specified API set is present on the current platform. Otherwise, this function returns **FALSE**.

A **TRUE** result reports that the API set is available in the composed API set schema on the running device. It isn't a guarantee that a particular file or export is present, or that a later call into the API set will succeed.

## -remarks

Windows editions share a common base of OS components that is called the *core OS* (in some contexts this is also called *OneCore*). In core OS components, Win32 APIs are organized into functional groups called [API sets](/windows/win32/apiindex/windows-apisets).

Some API sets aren't available on all Windows platforms. For example, although the full breadth of the Win32 API is supported on PCs, only a subset of the Win32 API is available on other devices such as HoloLens and Xbox. An API set can also be absent from an edition or device configuration where the feature that it represents has been removed.

When writing code that targets both desktop and non-desktop Windows devices, wrap the API call in **IsApiSetImplemented**. This function tests at run time if the API set that the API belongs to is present on the target platform. For more details see [Detect API set availability](/windows/win32/apiindex/detect-api-set-availability).

To identify whether a given Win32 API belongs to an API set, review the requirements table in the reference documentation for the API. If the API belongs to an API set, the requirements table in the article lists the API set name.

### Query forms

The *Contract* parameter takes one of these forms.

| API surface | Query form | Example |
|---|---|---|
| Named group | `<contract>~<group>` | `api-win-core-samplefeature~AdvancedOperations` |
| Default group | Contract alias, without `~Default` | `api-win-core-samplefeature` |
| Versioned contract | Complete versioned contract name | `ext-ms-win-core-samplefeature-l1-1-0` |

The `samplefeature` names are illustrative names for a fictional Windows component. The *Contract* prefix (`api-` or `ext-`) doesn't play a role in availability behavior.

Omit the `.dll` suffix. Use the suffix only when passing an API set name to a loader operation such as **LoadLibrary**.

For a named group, a **TRUE** result means that the group exists, its contract is mapped to an implementation module, that host is usable in the current execution environment, the group isn't disabled, and any system feature associated with the group is enabled. A query that passes a contract alias applies the contract and host checks.

The result is contract- or group-granular, not function-granular.

When an API's public header supplies an `Is<APIName>Present` helper, prefer that helper for a single optional API, because it already contains the correct name. Call **IsApiSetImplemented** directly when one decision guards several APIs, or when no helper is available. A helper is named for an API but its result is still group- or contract-granular, so two helpers backed by the same named group always agree.

### Calling an optional API

An availability query can protect process startup only if the optional target is delay-loaded or resolved dynamically. With a static import, the loader can fail the process before execution reaches the query.

1. Query the API set name, alias, or named group.
2. Enter the optional code path only when the query returns **TRUE**.
3. Load or call the target API.
4. Handle module-loading errors, missing exports, and the API's own documented failure results.

For a complete example, see [Detect API set availability](/windows/win32/apiindex/detect-api-set-availability). For delay-load configuration, see [Linker support for delay-loaded DLLs](/cpp/build/reference/linker-support-for-delay-loaded-dlls).

A versioned contract name gates APIs added in a later contract version; [GetApiSetModuleBaseName](./nf-apiquery2-getapisetmodulebasename.md) is an example.

### Linking

Include *apiquery2.h* and link one of the OneCore umbrella libraries. The choice is a trade-off between downlevel reach and directness of binding.

- *OneCore.lib* is the general-purpose choice. For this function it supplies a compatibility implementation that selects an API set query mechanism available on the running system, so the binary can also run on versions of Windows that predate the underlying support.
- *OneCore_apiset.lib* binds API set contract names directly, so no intermediate forwarding DLL is involved at run time. This is the most direct form, but a binary linked this way isn't guaranteed to run as-is on earlier versions of Windows. Choose it when the binary targets recent versions of Windows and you want direct binding for efficiency.

The declaration is available to the user-mode Desktop and System API partitions.

### Behavior on earlier versions of Windows

The compatibility implementation supplied by *OneCore.lib* still runs on a system where no API set query mechanism is available. In that case:

- A group-qualified name that contains `~` returns **FALSE**. A system that can't evaluate named groups can't report that a group is available.
- A name that isn't group-qualified can return **TRUE**. This preserves compatibility with applications that supplied their own forwarder DLLs on early versions of Windows, where the contract was in fact satisfied by that forwarder.

For this reason, treat the result as an availability signal rather than as a security boundary or a function-export test.

## -see-also

<a href="/windows/win32/apiindex/windows-apisets">Windows API sets</a>

<a href="/windows/win32/apiindex/detect-api-set-availability">Detect API set availability</a>

<a href="/windows/win32/api/apiquery2/nf-apiquery2-getapisetmodulebasename">GetApiSetModuleBaseName</a>

<a href="/windows-hardware/drivers/develop/building-for-onecore">Building for OneCore</a>

<a href="/windows-hardware/drivers/develop/validating-windows-drivers">Validating Windows drivers</a>
