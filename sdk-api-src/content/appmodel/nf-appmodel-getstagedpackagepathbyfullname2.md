---
UID: NF:appmodel.GetStagedPackagePathByFullName2
title: GetStagedPackagePathByFullName2
description: Gets the path of the specified staged package. (GetStagedPackagePathByFullName2)
helpviewer_keywords: ["GetStagedPackagePathByFullName2"]
tech.root: appxpkg
ms.date: 01/31/2019
ms.keywords: GetStagedPackagePathByFullName2
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: appmodel.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
targetos: Windows
ms.custom: 19H1
f1_keywords:
 - GetStagedPackagePathByFullName2
 - appmodel/GetStagedPackagePathByFullName2
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - api-ms-win-appmodel-runtime-l1-1-7.dll
 - api-ms-win-appmodel-runtime-l1-1-6.dll
 - api-ms-win-appmodel-runtime-l1-1-5.dll
 - api-ms-win-appmodel-runtime-l1-1-4.dll
 - api-ms-win-appmodel-runtime-l1-1-3.dll
 - appmodel.h
api_name:
 - GetStagedPackagePathByFullName2
---

# GetStagedPackagePathByFullName2 function


## -description

Gets the path of the specified staged package, with the option to specify the type of folder path to retrieve for the package.

## -parameters

### -param packageFullName

Type: <b>PCWSTR</b>

The full name of the staged package.

### -param packagePathType

Type: [**PackagePathType**](ne-appmodel-packagepathtype.md)

Indicates the type of folder path to retrieve for the package (the original install folder or the mutable folder).

### -param pathLength

Type: <b>UINT32*</b>

A pointer to a variable that holds the number of characters (<b>WCHAR</b>s) in the package path string, which includes the null-terminator. 

First you pass <b>NULL</b> to <i>path</i> to get the number of characters. You use this number to allocate memory space for <i>path</i>. Then you pass the address of this memory space to fill <i>path</i>.

### -param path

Type: <b>PWSTR</b>

A pointer to memory space that receives  the package path string, which includes the null-terminator.

## -returns

Type: <b>LONG</b>

If the function succeeds it returns <b>ERROR_SUCCESS</b>. Otherwise, the function returns an error code. The possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified by <i>path</i> is not large enough to hold the data. The required size is specified  by <i>pathLength</i>.

</td>
</tr>
</table>

## -remarks

The *packagePathType* parameter is useful for applications that use the [windows.mutablePackageDirectories extension](/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-package-extension) in their package manifest. This extension specifies a folder under the %ProgramFiles%\ModifiableWindowsApps path where the contents of the application's install folder are projected so that users can modify the installation files. This feature is currently available only for certain types of desktop PC games that are published by Microsoft and our partners, and it enables these types of games to support mods.

## -see-also

[GetStagedPackagePathByFullName](nf-appmodel-getstagedpackagepathbyfullname.md)
