---
UID: NF:appmodel.GetPackagePath
title: GetPackagePath function (appmodel.h)
description: Gets the path for the specified package.
helpviewer_keywords: ["GetPackagePath","GetPackagePath function [App packaging and management]","appmodel/GetPackagePath","appxpkg.getpackagepath"]
old-location: appxpkg\getpackagepath.htm
tech.root: appxpkg
ms.assetid: BDA0DD87-A36D-486B-BF89-EA5CC105C742
ms.date: 12/05/2018
ms.keywords: GetPackagePath, GetPackagePath function [App packaging and management], appmodel/GetPackagePath, appxpkg.getpackagepath
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
 - GetPackagePath
 - appmodel/GetPackagePath
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
 - GetPackagePath
---

# GetPackagePath function


## -description

Gets the path for the specified package.

## -parameters

### -param packageId [in]

Type: <b>const <a href="/windows/desktop/api/appmodel/ns-appmodel-package_id">PACKAGE_ID</a>*</b>

The package identifier.

### -param reserved

Type: <b>const UINT32</b>

Reserved, do not use.

### -param pathLength [in, out]

Type: <b>UINT32*</b>

On input, the size of the <i>path</i> buffer, in characters. On output, the size of the package path returned, in characters, including the null-terminator.

### -param path [out, optional]

Type: <b>PWSTR</b>

The package path.

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

## -see-also

<a href="/windows/desktop/api/appmodel/nf-appmodel-getpackageinfo">GetPackageInfo</a>