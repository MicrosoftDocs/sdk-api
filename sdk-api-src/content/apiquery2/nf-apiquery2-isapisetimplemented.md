---
UID: NF:apiquery2.IsApiSetImplemented
title: IsApiSetImplemented function (apiquery2.h)
description: The IsApiSetImplemented function tests if a specified API set is present on the computer.
helpviewer_keywords: ["IsApiSetImplemented","IsApiSetImplemented function [Windows API]","apiquery2/IsApiSetImplemented","winprog.isapisetimplemented"]
old-location: winprog\isapisetimplemented.htm
tech.root: winprog
ms.assetid: DF177716-9F33-4E39-BD63-D1B8E39CD67C
ms.date: 10/23/2020
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

Specifies the name of the API set to query. For more info, see the Remarks section.

## -returns

**IsApiSetImplemented** returns **TRUE** if the specified API set is present. In this case, APIs in the target API set have valid implementations on the current platform.

Otherwise, this function returns **FALSE**.

## -remarks

All versions of Windows 10 share a common base of OS components that is called the *core OS* (in some contexts this is also called *OneCore*). In core OS components, Win32 APIs are organized into functional groups called [API sets](/windows/win32/apiindex/windows-apisets).

Some API sets are not available on all Windows 10 platforms. For example, although the full breadth of the Win32 API is supported on PCs, only a subset of the Win32 API is available on other devices such as HoloLens, Xbox, and other devices running Windows 10x.

When writing code that targets both desktop and non-desktop Windows 10 devices, wrap the API call in **IsApiSetImplemented**. This function tests at runtime if the API set that the API belongs to is present on the target platform. For more details see [Detect API set availability](/windows/win32/apiindex/detect-api-set-availability).

To identify whether a given Win32 API belongs to an API set, review the requirements table in the reference documentation for the API. If the API belongs to an API set, the requirements table in the article lists the API set name.

## -see-also

<a href="/windows/win32/apiindex/windows-apisets">Windows API sets</a>

<a href="/windows/win32/apiindex/detect-api-set-availability">Detect API set availability</a>

<a href="/windows-hardware/drivers/develop/building-for-onecore">Building for OneCore</a>

<a href="/windows-hardware/drivers/develop/validating-universal-drivers">Validating Universal Windows drivers</a>
