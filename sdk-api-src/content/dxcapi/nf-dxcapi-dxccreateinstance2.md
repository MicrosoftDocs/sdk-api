---
UID: NF:dxcapi.DxcCreateInstance2
tech.root: direct3dhlsl
title: DxcCreateInstance2
ms.date: 04/05/2023
targetos: Windows
description: Creates a single uninitialized object of the class associated with a specified CLSID (can be used to create an instance of the compiler with a custom memory allocator).
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: dxcapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: dxcompiler.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dxcapi.h
api_name:
 - DxcCreateInstance2
f1_keywords:
 - DxcCreateInstance2
 - dxcapi/DxcCreateInstance2
dev_langs:
 - c++
helpviewer_keywords:
 - DxcCreateInstance2
---

## -description

Creates a single uninitialized object of the class associated with a specified CLSID (can be used to create an instance of the compiler with a custom memory allocator). Also see [DxcCreateInstance](./nf-dxcapi-dxccreateinstance.md).

## -parameters

### -param pMalloc

An **IMalloc** interface pointer representing a custom memory allocator.

### -param rclsid

The CLSID associated with the data and code that will be used to create the object.

### -param riid

A reference to the identifier of the interface to be used to communicate with the object.

### -param ppv

Address of pointer variable that receives the interface pointer requested in *riid*. Upon successful return, `*ppv` contains the requested interface pointer. Upon failure, `*ppv` contains NULL.

## -returns

While this function is similar to **CoCreateInstance**, there's no COM involvement.

## -remarks

To make it more convenient for you to use **GetProcAddress** to call **DxcCreateInstance2**, the **DxcCreateInstance2Proc** typedef is provided:

```cpp
typedef HRESULT(__stdcall *DxcCreateInstance2Proc)(
  _In_ IMalloc    *pMalloc,
  _In_ REFCLSID   rclsid,
  _In_ REFIID     riid,
  _Out_ LPVOID*   ppv
);
```

## -see-also
