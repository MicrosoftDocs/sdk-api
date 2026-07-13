---
UID: NF:appmodel.RemovePackageDependency
tech.root: appxpkg
title: RemovePackageDependency
ms.date: 7/12/2021
targetos: Windows
description: Removes a resolved package dependency from the current process' package graph (that is, a run-time reference for a framework package dependency that was added by using the AddPackageDependency function).
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
 - RemovePackageDependency
f1_keywords:
 - RemovePackageDependency
 - appmodel/RemovePackageDependency
dev_langs:
 - c++
---

## -description

Removes a resolved package dependency from the current process' package graph (that is, a run-time reference for a framework package dependency that was added by using the [AddPackageDependency](nf-appmodel-addpackagedependency.md) method).

## -parameters

### -param packageDependencyContext

Type: <b>PACKAGEDEPENDENCY_CONTEXT</b>

The handle of the package dependency to remove.

## -returns

Type: <b>HRESULT</b>

If the function succeeds it returns <b>ERROR_SUCCESS</b>. Otherwise, the function returns an error code. The possible error codes include the following.

| Return code | Description |
|-------------|-------------|
| E_INVALIDARG | The *packageDependencyContext* parameter is NULL on input. |

## -remarks

This function does not unload loaded resources such as DLLs. After removing a package dependency, any files loaded from the package can continue
to be used. Future file resolution will fail to see the removed package dependency.

## -see-also

[AddPackageDependency](nf-appmodel-addpackagedependency.md)
