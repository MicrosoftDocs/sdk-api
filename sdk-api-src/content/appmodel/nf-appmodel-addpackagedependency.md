---
UID: NF:appmodel.AddPackageDependency
title: AddPackageDependency
description: Resolves a previously defined PackageDependency to a specific package and adds it to the invoking process' package graph. After the dependency has been added, other code-loading methods (such as LoadLibrary and CoCreateInstance) can find the binaries in the resolved package.
ms.date: 7/12/2021
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
 - AddPackageDependency
f1_keywords:
 - AddPackageDependency
 - appmodel/AddPackageDependency
dev_langs:
 - c++
---

## -description

Adds a run-time reference for the framework package dependency you created earlier by using the [TryCreatePackageDependency](nf-appmodel-trycreatepackagedependency.md) method, with the specified options. After this method successfully returns, your app can activate types and use content from the framework package.

Also see [AddPackageDependency2](nf-appmodel-addpackagedependency2.md).

## -parameters

### -param packageDependencyId

Type: <b>PCWSTR</b>

The ID of the package dependency to be resolved and added to the invoking process' package graph. This parameter must match a package dependency defined by using the [TryCreatePackageDependency](nf-appmodel-trycreatepackagedependency.md) function for the calling user or the system (via the [CreatePackageDependencyOptions_ScopeIsSystem](ne-appmodel-createpackagedependencyoptions.md) option), or else an error is returned.

### -param rank

Type: <b>INT32</b>

The rank to use to add the resolved package to the caller's package graph. For more information, see the remarks.

### -param options

Type: <b><a href="ne-appmodel-addpackagedependencyoptions.md">AddPackageDependencyOptions</a></b>

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

Calling this method resolves the framework package dependency to a specific package on the system. It also informs the OS that the framework package is in active use and to handle any version updates in a side-by-side manner (effectively delay uninstalling or otherwise servicing the older version until after your app is done using it). Package resolution is specific to a user and can return different values for different users on a system.

Each successful **AddPackageDependency** call adds the resolved package to the calling process' package graph, even if already present. There is no duplicate detection or filtering applied by the API (that is, multiple references from a package is not harmful). After resolution is complete, the package dependency stays resolved for that user until the last reference across all processes for that user is removed via [RemovePackageDependency](nf-appmodel-removepackagedependency.md) or the process is terminated.

After this method successfully returns, your app can activate types and use content from the framework package until [RemovePackageDependency](nf-appmodel-removepackagedependency.md) is called.

If multiple packages are present in the package graph with the same rank as the call to **AddPackageDependency**, the resolved package is (by default) added after others of the same rank. To add a package before others of the same rank, specify [AddPackageDependencyOptions_PrependIfRankCollision](ne-appmodel-addpackagedependencyoptions.md) for the *options* parameter.

For more information, see [Use the dynamic dependency API to reference MSIX packages at run time](/windows/apps/desktop/modernize/framework-packages/use-the-dynamic-dependency-api).

## -see-also

* [RemovePackageDependency](./nf-appmodel-removepackagedependency.md)
* [TryCreatePackageDependency](./nf-appmodel-trycreatepackagedependency.md)
* [Use the dynamic dependency API to reference MSIX packages at run time](/windows/apps/desktop/modernize/framework-packages/use-the-dynamic-dependency-api)
