---
UID: NF:appmodel.DeletePackageDependency
tech.root: appxpkg
title: DeletePackageDependency
ms.date: 7/12/2021
targetos: Windows
description: Deletes the install-time reference for the framework package dependency you created earlier by using the TryCreatePackageDependency method. This method informs the OS that it is safe to remove the framework package if no other apps have a dependency on it.
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
 - DeletePackageDependency
f1_keywords:
 - DeletePackageDependency
 - appmodel/DeletePackageDependency
dev_langs:
 - c++
---

## -description

Deletes the install-time reference for the framework package dependency you created earlier by using the [TryCreatePackageDependency](nf-appmodel-trycreatepackagedependency.md) method. This method informs the OS that it is safe to remove the framework package if no other apps have a dependency on it.

## -parameters

### -param packageDependencyId

Type: <b>PCWSTR</b>

The ID of the package dependency to remove.

## -returns

| Return code | Description |
|-------------|-------------|
| E_INVALIDARG | The *packageDependencyId* parameter is NULL on input. |

## -remarks

Removing a package dependency is typically done when an app is uninstalled. A package dependency is implicitly removed if its lifetime artifact (specified via the *lifetimeArtifact* parameter of the [TryCreatePackageDependency](nf-appmodel-trycreatepackagedependency.md) function) is deleted. Package dependencies that are not referenced by other packages are elegible to be removed.

The caller of this function must have administrative privileges if the package dependency was created using [CreatePackageDependencyOptions_ScopeIsSystem](ne-appmodel-createpackagedependencyoptions.md).

## -see-also

[TryCreatePackageDependency](nf-appmodel-trycreatepackagedependency.md)


[Use the dynamic dependency API to reference MSIX packages at run time](/windows/apps/desktop/modernize/framework-packages/use-the-dynamic-dependency-api)
