---
UID: NF:appmodel.GetResolvedPackageFullNameForPackageDependency
tech.root: appxpkg
title: GetResolvedPackageFullNameForPackageDependency
ms.date: 7/12/2021
targetos: Windows
description: Returns the package full name that would be used if the package dependency were to be resolved. This function does not add the package to the process graph.
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
req.lib: 
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
 - GetResolvedPackageFullNameForPackageDependency
f1_keywords:
 - GetResolvedPackageFullNameForPackageDependency
 - appmodel/GetResolvedPackageFullNameForPackageDependency
dev_langs:
 - c++
---

## -description

Returns the package full name that would be used if the package dependency were to be resolved. This function does not add the package to the invoking process' package graph.

## -parameters

### -param packageDependencyId

Type: <b>PCWSTR</b>

The ID of the package dependency to be resolved. This parameter must match a package dependency defined by using the [TryCreatePackageDependency](nf-appmodel-trycreatepackagedependency.md) function for the calling user or the system (via the [CreatePackageDependencyOptions_ScopeIsSystem](ne-appmodel-createpackagedependencyoptions.md) option), or else an error is returned.

### -param packageFullName

Type: <b>PCWSTR*</b>

The full name of the package to which the dependency has been resolved. If the package dependency cannot be resolved, the function succeeds but this parameter is **nullptr** on output. Use the [HeapAlloc](/windows/win32/api/heapapi/nf-heapapi-heapalloc) function to allocate memory for this parameter, and use [HeapFree](/windows/win32/api/heapapi/nf-heapapi-heapfree) to deallocate the memory.

## -returns

| Return code | Description |
|-------------|-------------|
| E_INVALIDARG | The *packageDependencyId* or *packageFullName* parameter is NULL on input. |

## -remarks

To add the package to the invoking process' package graph, use the [AddPackageDependency](nf-appmodel-addpackagedependency.md) function.

## -see-also

[TryCreatePackageDependency](nf-appmodel-trycreatepackagedependency.md)


[AddPackageDependency](nf-appmodel-addpackagedependency.md)
