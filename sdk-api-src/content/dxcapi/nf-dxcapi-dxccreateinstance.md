---
UID: NF:dxcapi.DxcCreateInstance
tech.root: direct3dhlsl
title: DxcCreateInstance
ms.date: 04/05/2023
targetos: Windows
description: Creates a single uninitialized object of the class associated with a specified CLSID.
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
 - DxcCreateInstance
f1_keywords:
 - DxcCreateInstance
 - dxcapi/DxcCreateInstance
dev_langs:
 - c++
helpviewer_keywords:
 - DxcCreateInstance
---

## -description

Creates a single uninitialized object of the class associated with a specified CLSID. Also see [DxcCreateInstance2](./nf-dxcapi-dxccreateinstance2.md).

## -parameters

### -param rclsid

The CLSID associated with the data and code that will be used to create the object.

### -param riid

A reference to the identifier of the interface to be used to communicate with the object.

### -param ppv

Address of pointer variable that receives the interface pointer requested in *riid*. Upon successful return, `*ppv` contains the requested interface pointer. Upon failure, `*ppv` contains NULL.

## -returns

While this function is similar to **CoCreateInstance**, there's no COM involvement.

## -remarks

To make it more convenient for you to use **GetProcAddress** to call **DxcCreateInstance**, the **DxcCreateInstanceProc** typedef is provided:

```cpp
typedef HRESULT (__stdcall *DxcCreateInstanceProc)(
  _In_ REFCLSID   rclsid,
  _In_ REFIID     riid,
  _Out_ LPVOID*   ppv
);
```

## -see-also
