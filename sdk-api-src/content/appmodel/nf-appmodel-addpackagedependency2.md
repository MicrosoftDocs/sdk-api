---
UID: NF:appmodel.AddPackageDependency2
title: AddPackageDependency2
description: Resolves a previously defined package dependency to a specific package, and adds it to the invoking process' package graph. After the dependency has been added, other code-loading methods (such as LoadLibrary and CoCreateInstance) can find the binaries in the resolved package.
ms.date: 02/05/2025
tech.root: appxpkg
targetos: Windows
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
req.target-min-winverclnt: Windows 11, version 23H2 (10.0; Build 22631)
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
 - appmodel.h
api_name:
 - AddPackageDependency2
f1_keywords:
 - AddPackageDependency2
 - appmodel/AddPackageDependency2
dev_langs:
 - c++
---

## -description

Adds a run-time reference for the framework package dependency you created earlier by using the [TryCreatePackageDependency](./nf-appmodel-trycreatepackagedependency.md) method, with the specified options. After this method successfully returns, your app can activate types and use content from the framework package.

## -parameters

### -param packageDependencyId

Type: <b>PCWSTR</b>

The ID of the package dependency to be resolved and added to the invoking process' package graph. This parameter must match a package dependency defined by using the [TryCreatePackageDependency](nf-appmodel-trycreatepackagedependency.md) function for the calling user or the system (via the [CreatePackageDependencyOptions_ScopeIsSystem](ne-appmodel-createpackagedependencyoptions.md) option), or else an error is returned.

### -param rank

Type: <b>INT32</b>

The rank to use to add the resolved package to the caller's package graph. For more information, see **Remarks**.

### -param options

Type: <b><a href="./ne-appmodel-addpackagedependencyoptions2.md">AddPackageDependencyOptions2</a></b>

The options to apply when adding the package dependency.

### -param packageDependencyContext

Type: <b>PACKAGEDEPENDENCY_CONTEXT*</b>

The handle of the added package dependency. This handle is valid until it is passed to <a href="nf-appmodel-removepackagedependency.md">RemovePackageDependency</a>.

### -param packageFullName

Type: <b>PCWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated Unicode string that specifies the full name of the package to which the dependency has been resolved. The caller is responsible for freeing this resource once it is no longer needed by calling [HeapFree](/windows/win32/api/heapapi/nf-heapapi-heapfree).

## -returns

Type: <b>HRESULT</b>

If the function succeeds it returns <b>ERROR_SUCCESS</b>. Otherwise, the function returns an error code. The possible error codes include the following.

| Return code | Description |
|-------------|-------------|
| E_INVALIDARG | The *packageDependencyId* or *packageDependencyContext* parameter is NULL on input. |

## -remarks

See **Remarks** for [AddPackageDependency](./nf-appmodel-addpackagedependency.md).

## -see-also

* [RemovePackageDependency](./nf-appmodel-removepackagedependency.md)
* [TryCreatePackageDependency](./nf-appmodel-trycreatepackagedependency.md)
* [Use the dynamic dependency API to reference MSIX packages at run time](/windows/apps/desktop/modernize/framework-packages/use-the-dynamic-dependency-api)
