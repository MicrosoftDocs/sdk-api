---
UID: NF:appmodel.GetStagedPackageOrigin
title: GetStagedPackageOrigin function (appmodel.h)
description: Gets the origin of the specified package.
helpviewer_keywords: ["GetStagedPackageOrigin","GetStagedPackageOrigin function [App packaging and management]","appmodel/GetStagedPackageOrigin","appxpkg.getstagedpackageorigin"]
old-location: appxpkg\getstagedpackageorigin.htm
tech.root: appxpkg
ms.assetid: 7A1EE2CA-83CE-4E03-85A5-0061E29EB49B
ms.date: 12/05/2018
ms.keywords: GetStagedPackageOrigin, GetStagedPackageOrigin function [App packaging and management], appmodel/GetStagedPackageOrigin, appxpkg.getstagedpackageorigin
req.header: appmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: onecoreuap.lib
req.dll: Kernelbase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetStagedPackageOrigin
 - appmodel/GetStagedPackageOrigin
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
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - Kernel.AppCore.dll
 - Ext-MS-Win-Kernel32-package-l1-1-2.dll
 - ext-ms-win-kernel32-package-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - GetStagedPackageOrigin
---

# GetStagedPackageOrigin function


## -description

Gets the origin of the specified package.

## -parameters

### -param packageFullName [in]

Type: <b>PCWSTR</b>

The full name of the package.

### -param origin [out]

Type: <b><a href="/windows/desktop/api/appmodel/ne-appmodel-packageorigin">PackageOrigin</a>*</b>

A pointer to a variable that receives a <a href="/windows/desktop/api/appmodel/ne-appmodel-packageorigin">PackageOrigin</a>-typed value that indicates the origin of the package specified by <i>packageFullName</i>.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>packageFullName</i> parameter isn't valid.

</td>
</tr>
</table>
