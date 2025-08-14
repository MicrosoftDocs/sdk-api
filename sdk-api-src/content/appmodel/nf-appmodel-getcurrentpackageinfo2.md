---
UID: NF:appmodel.GetCurrentPackageInfo2
title: GetCurrentPackageInfo2
description: Gets the package information for the calling process. (GetCurrentPackageInfo2)
helpviewer_keywords: ["GetCurrentPackageInfo2"]
tech.root: appxpkg
ms.date: 01/31/2019
ms.keywords: GetCurrentPackageInfo2
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: kernelbase.dll
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
req.typenames: 
req.umdf-ver: 
req.unicode-ansi: 
targetos: Windows
ms.custom: 19H1
f1_keywords:
 - GetCurrentPackageInfo2
 - appmodel/GetCurrentPackageInfo2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-appmodel-runtime-l1-1-7.dll
 - api-ms-win-appmodel-runtime-l1-1-6.dll
 - api-ms-win-appmodel-runtime-l1-1-5.dll
 - api-ms-win-appmodel-runtime-l1-1-4.dll
 - api-ms-win-appmodel-runtime-l1-1-3.dll
 - kernelbase.dll
api_name:
 - GetCurrentPackageInfo2
---

# GetCurrentPackageInfo2 function


## -description

Gets the package information for the calling process, with the option to specify the type of folder path to retrieve for the package.

## -parameters

### -param flags

Type: <b>const UINT32</b>

The [package constants](/windows/desktop/appxpkg/package-constants) that specify how package information is retrieved. The <b>PACKAGE_FILTER_*</b> flags are supported.

### -param packagePathType

Type: [**PackagePathType**](ne-appmodel-packagepathtype.md)

Indicates the type of folder path to retrieve for the package (the original install folder or the mutable folder).

### -param bufferLength

Type: <b>UINT32*</b>

On input, the size of <i>buffer</i>, in bytes. On output, the size of the array of structures returned, in bytes.

### -param buffer

Type: <b>BYTE*</b>

The package information, represented as an array of <a href="/windows/desktop/api/appmodel/ns-appmodel-package_info">PACKAGE_INFO</a> structures.

### -param count

Type: <b>UINT32*</b>

The number of structures in the buffer.

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
<dt><b>APPMODEL_ERROR_NO_PACKAGE</b></dt>
</dl>
</td>
<td width="60%">
The process has no package identity.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to hold the data. The required size is specified  by <i>bufferLength</i>.

</td>
</tr>
</table>

## -remarks

The *packagePathType* parameter is useful for applications that use the [windows.mutablePackageDirectories extension](/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-package-extension) in their package manifest. This extension specifies a folder under the %ProgramFiles%\ModifiableWindowsApps path where the contents of the application's install folder are projected so that users can modify the installation files. This feature is currently available only for certain types of desktop PC games that are published by Microsoft and our partners, and it enables these types of games to support mods.

## -see-also

[GetCurrentPackageInfo](nf-appmodel-getcurrentpackageinfo.md)



<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackagefamilyname">GetCurrentPackageFamilyName</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackagefullname">GetCurrentPackageFullName</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackageid">GetCurrentPackageId</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackagepath">GetCurrentPackagePath</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getpackageinfo">GetPackageInfo</a>



[GetPackageInfo2](nf-appmodel-getpackageinfo2.md)
