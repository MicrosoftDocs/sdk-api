---
UID: NF:winternl.NtQueryMultipleValueKey
title: NtQueryMultipleValueKey function (winternl.h)
description: Retrieves values for the specified multiple-value key.
helpviewer_keywords: ["NtQueryMultipleValueKey","NtQueryMultipleValueKey function [Windows API]","base.ntquerymultiplevaluekey","winprog.ntquerymultiplevaluekey","winternl/NtQueryMultipleValueKey"]
old-location: winprog\ntquerymultiplevaluekey.htm
tech.root: winprog
ms.assetid: fe78446c-b936-4ded-846a-f3ca26eff06e
ms.date: 12/05/2018
ms.keywords: NtQueryMultipleValueKey, NtQueryMultipleValueKey function [Windows API], base.ntquerymultiplevaluekey, winprog.ntquerymultiplevaluekey, winternl/NtQueryMultipleValueKey
req.header: winternl.h
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
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NtQueryMultipleValueKey
 - winternl/NtQueryMultipleValueKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ntdll.dll
api_name:
 - NtQueryMultipleValueKey
---

# NtQueryMultipleValueKey function


## -description

<p class="CCE_Message">[This function may be changed or removed from Windows without further notice.]

Retrieves values for the specified multiple-value key.

## -parameters

### -param KeyHandle [in]

A handle to the key for which to retrieve values. The handle must be opened with the <b>KEY_QUERY_VALUE</b> access right.

### -param ValueEntries [in, out]

A pointer to an array of [**KEY_VALUE_ENTRY**] structures containing the names of values to retrieve.

### -param EntryCount [in]

The number of elements in the <i>ValueEntries</i> array.

### -param ValueBuffer [out]

A pointer to a buffer to receive the values.

### -param BufferLength [in, out]

A pointer to a variable that contains the size of the buffer at <i>ValueBuffer</i>, in bytes. When the function returns, the <i>BufferLength</i> parameter contains the number of bytes written to the buffer at <i>ValueBuffer</i>.

### -param RequiredBufferLength [out, optional]

A pointer to a variable to receive the number of bytes required for all of the values to be returned by the function. This parameter can be <b>NULL</b>.

## -returns

Returns an <b>NTSTATUS</b> or error code.

If the buffer is too small to hold the information to be retrieved, the function returns <b>STATUS_BUFFER_OVERFLOW</b> and, if the <i>RequiredBufferLength</i> parameter is specified, sets it to the buffer size required.

The forms and significance of <b>NTSTATUS</b> error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.

## -remarks

This function has no associated header file. You can also use the <a href="/windows/desktop/DevNotes/-loadlibrary">LoadLibrary</a> and <a href="/windows/desktop/DevNotes/-getprocaddress-">GetProcAddress</a> functions to dynamically link to Ntdll.dll.

## -see-also

<a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>