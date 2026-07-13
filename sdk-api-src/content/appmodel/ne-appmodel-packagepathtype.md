---
UID: NE:appmodel.PackagePathType
title: PackagePathType
description: Indicates the type of package folder to retrieve.
helpviewer_keywords: ["PackagePathType"]
tech.root: appxpkg
ms.date: 01/27/2026
ms.keywords: PackagePathType
req.construct-type: enumeration
req.ddi-compliance: 
req.header: appmodel.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.target-type: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.typenames: 
req.umdf-ver: 
targetos: Windows
ms.custom: 19H1
f1_keywords:
 - PackagePathType
 - appmodel/PackagePathType
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - appmodel.h
api_name:
 - PackagePathType
---

## -description

Indicates the type of folder path to retrieve in a query for the path or other info about a package.

## -enum-fields

### -field PackagePathType_Install

Retrieve the package's install path.

### -field PackagePathType_Mutable

If the package has a [Mutable location](/uwp/schemas/appxpackage/uapmanifestschema/element-desktop8-mutablepackagedirectories), then retrieve the package's Mutable path.

### -field PackagePathType_Effective

Specifies that the package path should be retrieved according to the following logic:

* If the package has a User-External location, then return that path.
* Otherwise, if the package has a Machine-External location, then return that path.
* Otherwise, if the package has a [Mutable location](/uwp/schemas/appxpackage/uapmanifestschema/element-desktop8-mutablepackagedirectories), then return the Mutable path. Also see [Create a directory in any location based on packaged app directory](/windows/msix/manage/create-directory).
* Otherwise, return the package's Install path.

### -field PackagePathType_MachineExternal

Specifies that the package path should be retrieved according to the following logic:

* If the package has a Machine-External location, then return that path.
* Otherwise, return an error.

### -field PackagePathType_UserExternal

Specifies that the package path should be retrieved according to the following logic:

* If the package has a User-External location, then return that path.
* Otherwise, return an error.

### -field PackagePathType_EffectiveExternal

Specifies that the package path should be retrieved according to the following logic:

* If the package has a User-External location, then return that path.
* Otherwise, if the package has a Machine-External location, then return that path.
* Otherwise, return an error.

## -remarks

An application has a mutable install folder if it uses the [windows.mutablePackageDirectories extension](/uwp/schemas/appxpackage/uapmanifestschema/element-desktop8-mutablepackagedirectories) in its package manifest. This extension specifies a folder under the %ProgramFiles%\ModifiableWindowsApps path where the contents of the application's install folder are projected so that users can modify the installation files.

> [!IMPORTANT]
> This feature requires the **modifiableApp** [restricted capability](/windows/uwp/packaging/app-capability-declarations). Microsoft Store policy requires packages with that capability to be certain types of desktop PC games that are published by Microsoft and its partners.

A package always has an Install location. A package can also have a Mutable, Machine External and/or User External location.

The concept of "effective" is the location that has the highest precedence for the package/user.

## -see-also

* [GetCurrentPackageInfo2](nf-appmodel-getcurrentpackageinfo2.md)
* [GetCurrentPackagePath2](nf-appmodel-getcurrentpackagepath2.md)
* [GetPackagePathByFullName2](nf-appmodel-getpackagepathbyfullname2.md)
* [GetPackageInfo2](nf-appmodel-getpackageinfo2.md)
* [GetStagedPackagePathByFullName2](nf-appmodel-getstagedpackagepathbyfullname2.md)
* [desktop6:MutablePackageDirectories](/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectories)
* [desktop8:MutablePackageDirectories](/uwp/schemas/appxpackage/uapmanifestschema/element-desktop8-mutablepackagedirectories)
* [Package.MutableLocation property](/uwp/api/windows.applicationmodel.package.mutablelocation)
* [Package.MutablePath property](/uwp/api/windows.applicationmodel.package.mutablepath)
