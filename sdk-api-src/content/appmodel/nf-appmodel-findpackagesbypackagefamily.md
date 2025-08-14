---
UID: NF:appmodel.FindPackagesByPackageFamily
title: FindPackagesByPackageFamily function (appmodel.h)
description: Finds the packages with the specified family name for the current user.
helpviewer_keywords: ["FindPackagesByPackageFamily","FindPackagesByPackageFamily function [App packaging and management]","appmodel/FindPackagesByPackageFamily","appxpkg.findpackagesbypackagefamily"]
old-location: appxpkg\findpackagesbypackagefamily.htm
tech.root: appxpkg
ms.assetid: D52E98BD-726F-4AC0-A034-02896B1D1687
ms.date: 12/05/2018
ms.keywords: FindPackagesByPackageFamily, FindPackagesByPackageFamily function [App packaging and management], appmodel/FindPackagesByPackageFamily, appxpkg.findpackagesbypackagefamily
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FindPackagesByPackageFamily
 - appmodel/FindPackagesByPackageFamily
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
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - FindPackagesByPackageFamily
---

# FindPackagesByPackageFamily function


## -description

Finds the packages  with the specified family name for the current user.

## -parameters

### -param packageFamilyName [in]

Type: <b>PCWSTR</b>

The package family name.

### -param packageFilters [in]

Type: <b>UINT32</b>

The <a href="/windows/desktop/appxpkg/package-constants">package constants</a> that specify how package information is retrieved. All package constants except <b>PACKAGE_FILTER_ALL_LOADED</b> are supported.

### -param count [in, out]

Type: <b>UINT32*</b>

A pointer to a variable that holds the number of package full names that were found. 

First you pass <b>NULL</b> to <i>packageFullNames</i> to get the number of package full names that were found. You use this number to allocate memory space for <i>packageFullNames</i>. Then you pass the address of this memory space to fill <i>packageFullNames</i>.

### -param packageFullNames [out, optional]

Type: <b>PWSTR*</b>

A pointer to memory space that receives  the strings of package full names that were found.

### -param bufferLength [in, out]

Type: <b>UINT32*</b>

A pointer to a variable that holds the number of characters in the string of package full names. 

First you pass <b>NULL</b> to <i>buffer</i> to get the number of characters. You use this number to allocate memory space for <i>buffer</i>. Then you pass the address of this memory space to fill <i>buffer</i>.

### -param buffer [out, optional]

Type: <b>WCHAR*</b>

A pointer to memory space that receives  the string of characters for all of the package full names.

### -param packageProperties [out, optional]

Type: <b>UINT32*</b>

A pointer to memory space that receives  the <a href="/windows/desktop/appxpkg/package-constants">package properties</a> for all of the packages that were found.

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
One or more buffer is not large enough to hold the data. The required size is specified  by either <i>count</i> or <i>buffer</i>.

</td>
</tr>
</table>