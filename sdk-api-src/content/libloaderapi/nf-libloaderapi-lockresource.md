---
UID: NF:libloaderapi.LockResource
title: LockResource function (libloaderapi.h)
description: Retrieves a pointer to the specified resource in memory.
helpviewer_keywords: ["LockResource","LockResource function [Menus and Other Resources]","_win32_LockResource","_win32_lockresource_cpp","libloaderapi/LockResource","menurc.lockresource","winui._win32_lockresource"]
old-location: menurc\lockresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\lockresource.htm
ms.date: 09/24/2020
ms.keywords: LockResource, LockResource function [Menus and Other Resources], _win32_LockResource, _win32_lockresource_cpp, libloaderapi/LockResource, menurc.lockresource, winui._win32_lockresource
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LockResource
 - libloaderapi/LockResource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-libraryloader-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-1.dll
 - API-MS-Win-Core-LibraryLoader-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - LockResource
---

# LockResource function


## -description

Retrieves a pointer to the specified resource in memory.

## -parameters

### -param hResData [in]

Type: **HGLOBAL**

A handle to the resource to be accessed. The [LoadResource function](nf-libloaderapi-loadresource.md) returns this handle. Note that this parameter is listed as an **HGLOBAL** variable only for backward compatibility. Do not pass any value as a parameter other than a successful return value from the **LoadResource** function.

## -returns

Type: **LPVOID**

If the loaded resource is available, the return value is a pointer to the first byte of the resource; otherwise, it is **NULL**.

## -remarks

The pointer returned by **LockResource** is valid until the module containing the resource is unloaded. It is not necessary to unlock resources because the system automatically deletes them when the process that created them terminates.

Do not try to lock a resource by using the handle returned by the [FindResourceA function](../winbase/nf-winbase-findresourcea.md) or [FindResourceExA function](../winbase/nf-winbase-findresourceexa.md) function. Such a handle points to random data. 

> [!Note]
> **LockResource** does not actually lock memory; it is just used to obtain a pointer to the memory containing the resource data. The name of the function comes from versions prior to Windows XP, when it was used to lock a global memory block allocated by [LoadResource](nf-libloaderapi-loadresource.md).

#### Examples

For an example, see [Updating Resources](/windows/win32/menurc/using-resources#updating-resources).

## -see-also

### Conceptual

- [Resources](/windows/win32/menurc/resources)

### Reference

- [Menus and Other Resources](../_menurc/index.md)
- [FindResourceA function](../winbase/nf-winbase-findresourcea.md)
= [FindResourceExA function](../winbase/nf-winbase-findresourceexa.md)
- [LoadResource function](nf-libloaderapi-loadresource.md)