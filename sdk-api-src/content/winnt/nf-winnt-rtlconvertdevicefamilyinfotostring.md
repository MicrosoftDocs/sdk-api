---
UID: NF:winnt.RtlConvertDeviceFamilyInfoToString
title: RtlConvertDeviceFamilyInfoToString
description: Retrieves string representations of device family info.
tech.root: Debug
ms.date: 03/31/2023
prerelease: false
req.construct-type: function
req.header: winnt.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: Windows 10, version 1903
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
 - RtlConvertDeviceFamilyInfoToString
 - winnt/RtlConvertDeviceFamilyInfoToString
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - NtDll.dll
api_name:
 - RtlConvertDeviceFamilyInfoToString
helpviewer_keywords:
 - RtlConvertDeviceFamilyInfoToString
---

## -description

Retrieves string representations of device family info.

## -parameters

### -param pulDeviceFamilyBufferSize

Type: _Inout_ **PDWORD**

The size of the buffer for the device family.

### -param pulDeviceFormBufferSize

Type: _Inout_ **PDWORD**

The size of the buffer for the device form.

### -param DeviceFamily

Type: _Out_writes_bytes_(*pulDeviceFamilyBufferSize) **PWSTR**

The retrieved device family.

### -param DeviceForm

Type: _Out_writes_bytes_(*pulDeviceFormBufferSize) **PWSTR**

The retrieved device form.

## -returns

Type: DWORD

A success or failure status.

## -remarks

At this time, this function doesn't have an associated library file. Your application can call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (`NtDll.dll`) to obtain a module handle. It can then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with the module handle and the name of this function to get the function address.

## -see-also
