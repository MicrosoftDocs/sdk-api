---
UID: NF:appmodel.OpenPackageInfoByFullName
title: OpenPackageInfoByFullName function (appmodel.h)
description: Opens the package information of the specified package.
helpviewer_keywords: ["OpenPackageInfoByFullName","OpenPackageInfoByFullName function [App packaging and management]","appmodel/OpenPackageInfoByFullName","appxpkg.openpackageinfobyfullname"]
old-location: appxpkg\openpackageinfobyfullname.htm
tech.root: appxpkg
ms.assetid: 9ECFC757-1CB3-43A1-BA45-9AF72CAB240E
ms.date: 12/05/2018
ms.keywords: OpenPackageInfoByFullName, OpenPackageInfoByFullName function [App packaging and management], appmodel/OpenPackageInfoByFullName, appxpkg.openpackageinfobyfullname
req.header: appmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OpenPackageInfoByFullName
 - appmodel/OpenPackageInfoByFullName
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
 - Kernel32.dll
 - API-MS-Win-AppModel-Runtime-l1-1-0.dll
 - kernel32legacy.dll
 - Ext-MS-Win-kernel32-package-l1-1-0.dll
 - Kernel.AppCore.dll
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - Ext-MS-Win-Kernel32-package-l1-1-2.dll
 - ext-ms-win-kernel32-package-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - OpenPackageInfoByFullName
---

# OpenPackageInfoByFullName function


## -description

Opens the package information of the specified package.

## -parameters

### -param packageFullName [in]

Type: <b>PCWSTR</b>

The full name of the package.

### -param reserved

Type: <b>const UINT32</b>

Reserved; must be 0.

### -param packageInfoReference [out]

Type: <b>PACKAGE_INFO_REFERENCE*</b>

A reference to package information.

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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The package is not installed for the current user.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/appmodel/nf-appmodel-closepackageinfo">ClosePackageInfo</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getpackageinfo">GetPackageInfo</a>