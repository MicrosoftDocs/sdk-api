---
UID: NF:appmodel.GetPackageInfo
title: GetPackageInfo function (appmodel.h)
description: Gets the package information for the specified package. (GetPackageInfo)
helpviewer_keywords: ["GetPackageInfo","GetPackageInfo function [App packaging and management]","appmodel/GetPackageInfo","appxpkg.getpackageinfo"]
old-location: appxpkg\getpackageinfo.htm
tech.root: appxpkg
ms.assetid: 28F45B3B-A61F-44D3-B606-6966AD5866FA
ms.date: 12/05/2018
ms.keywords: GetPackageInfo, GetPackageInfo function [App packaging and management], appmodel/GetPackageInfo, appxpkg.getpackageinfo
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
 - GetPackageInfo
 - appmodel/GetPackageInfo
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
 - GetPackageInfo
---

# GetPackageInfo function


## -description

Gets the package information for the specified package.

## -parameters

### -param packageInfoReference [in]

Type: <b>PACKAGE_INFO_REFERENCE</b>

A reference to package information.

### -param flags [in]

Type: <b>const UINT32</b>

The <a href="/windows/desktop/appxpkg/package-constants">package constants</a> that specify how package information is retrieved.

### -param bufferLength [in, out]

Type: <b>UINT32*</b>

On input, the size of <i>buffer</i>, in bytes. On output, the size of the package information returned, in bytes.

### -param buffer [out, optional]

Type: <b>BYTE*</b>

The package information, represented as an array of <a href="/windows/desktop/api/appmodel/ns-appmodel-package_info">PACKAGE_INFO</a> structures.

### -param count [out, optional]

Type: <b>UINT32*</b>

The number of packages in the buffer.

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
The buffer is not large enough to hold the data. The required size is specified  by <i>bufferLength</i>.

</td>
</tr>
</table>

## -see-also

[GetPackageInfo2](nf-appmodel-getpackageinfo2.md)


<a href="/windows/desktop/api/appmodel/nf-appmodel-closepackageinfo">ClosePackageInfo</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackageinfo">GetCurrentPackageInfo</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getpackagepath">GetPackagePath</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-openpackageinfobyfullname">OpenPackageInfoByFullName</a>
