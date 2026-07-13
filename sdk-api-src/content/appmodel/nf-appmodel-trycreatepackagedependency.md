---
UID: NF:appmodel.TryCreatePackageDependency
tech.root: appxpkg
title: TryCreatePackageDependency
ms.date: 7/12/2021
targetos: Windows
description: Creates an install-time reference for a framework package dependency for the current app, using the specified package family name, minimum version, and additional criteria.
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
 - TryCreatePackageDependency
f1_keywords:
 - TryCreatePackageDependency
 - appmodel/TryCreatePackageDependency
dev_langs:
 - c++
---

## -description

Creates an install-time reference for a framework package dependency for the current app, using the specified package family name, minimum version, and additional criteria.

## -parameters

### -param user

Type: <b>PSID</b>

The user scope of the package dependency. If NULL, the caller's user context is used. Must be NULL if [CreatePackageDependencyOptions_ScopeIsSystem](ne-appmodel-createpackagedependencyoptions.md) is specified.

### -param packageFamilyName

Type: <b>PCWSTR</b>

The package family name of the framework package on which to take dependency.

### -param minVersion

Type: <b><a href="/windows/desktop/api/appmodel/ns-appmodel-package_version">PACKAGE_VERSION</a></b>

The minimum version of the framework package on which to take dependency.

### -param packageDependencyProcessorArchitectures

Type: <b><a href="ne-appmodel-packagedependencyprocessorarchitectures.md">PackageDependencyProcessorArchitectures</a></b>

The processor architectures of the package dependency.

### -param lifetimeKind

Type: <b><a href="ne-appmodel-packagedependencylifetimekind.md">PackageDependencyLifetimeKind</a></b>

The type of artifact to use to define the lifetime of the package dependency. For more information, see the remarks.

### -param lifetimeArtifact

Type: <b>PCWSTR</b>

The name of the artifact used to define the lifetime of the package dependency. Must be NULL if the *lifetimeKind* parameter is [PackageDependencyLifetimeKind_Process](ne-appmodel-packagedependencylifetimekind.md). For more information, see the remarks.

### -param options

Type: <b><a href="ne-appmodel-createpackagedependencyoptions.md">CreatePackageDependencyOptions</a></b>

The options to apply when creating the package dependency.

### -param packageDependencyId

Type: <b>PWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated Unicode string that specifies the ID of the new package dependency. The caller is responsible for freeing this resource once it is no longer needed by calling [HeapFree](/windows/win32/api/heapapi/nf-heapapi-heapfree).

## -returns

Type: <b>HRESULT</b>

If the function succeeds it returns <b>ERROR_SUCCESS</b>. Otherwise, the function returns an error code. The possible error codes include the following.

| Return code | Description |
|-------------|-------------|
| E_INVALIDARG | The *packageDependencyId* parameter is NULL on input. |

## -remarks

In your app's installer or during the first run of your app, call this method to specify a set of criteria for a framework package you want to use in your app. This informs the OS that your app has a dependency upon a framework package that meets the specified criteria. If one or more framework packages are installed that meet the criteria, Windows will ensure that at least one of these framework packages will remain installed until the install-time reference is deleted. For more information, see [Use the dynamic dependency API to reference MSIX packages at run time](/windows/apps/desktop/modernize/framework-packages/use-the-dynamic-dependency-api).

This function fails if the specified dependency criteria cannot be resolved to a specific package. This package resolution check is skipped if [CreatePackageDependencyOptions_DoNotVerifyDependencyResolution](ne-appmodel-createpackagedependencyoptions.md) is specified for the *options* parameter. This is useful for installers running as user contexts other than the target user (for example, installers running as LocalSystem).

## -see-also

[Use the dynamic dependency API to reference MSIX packages at run time](/windows/apps/desktop/modernize/framework-packages/use-the-dynamic-dependency-api)
