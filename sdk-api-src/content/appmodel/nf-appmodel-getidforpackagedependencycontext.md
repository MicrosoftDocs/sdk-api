---
UID: NF:appmodel.GetIdForPackageDependencyContext
tech.root: appxpkg
title: GetIdForPackageDependencyContext
ms.date: 7/12/2021
targetos: Windows
description: Returns the package dependency for the specified context handle.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: appmodel.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: OneCoreUAP.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 (introduced in 10.0.22000.0)
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
 - api-ms-win-appmodel-runtime-l1-1-7.dll
 - api-ms-win-appmodel-runtime-l1-1-6.dll
 - api-ms-win-appmodel-runtime-l1-1-5.dll
 - appmodel.h
api_name:
 - GetIdForPackageDependencyContext
f1_keywords:
 - GetIdForPackageDependencyContext
 - appmodel/GetIdForPackageDependencyContext
dev_langs:
 - c++
---

## -description

Returns the package dependency for the specified context handle.

## -parameters

### -param packageDependencyContext

Type: <b>PACKAGEDEPENDENCY_CONTEXT</b>

The handle of the package dependency to return.

### -param packageDependencyId

Type: <b>PCWSTR*</b>

The ID of the package dependency for the specified context handle. If the package dependency cannot be resolved, the function succeeds but this parameter is **nullptr** on output. Use the [HeapAlloc](/windows/win32/api/heapapi/nf-heapapi-heapalloc) function to allocate memory for this parameter, and use [HeapFree](/windows/win32/api/heapapi/nf-heapapi-heapfree) to deallocate the memory.

## -returns

| Return code | Description |
|-------------|-------------|
| E_INVALIDARG | The *packageDependencyContext* or *packageDependencyId* parameter is NULL on input. |

## -remarks

## -see-also
