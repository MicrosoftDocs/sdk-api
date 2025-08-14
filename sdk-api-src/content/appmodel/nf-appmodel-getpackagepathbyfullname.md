---
UID: NF:appmodel.GetPackagePathByFullName
title: GetPackagePathByFullName function (appmodel.h)
description: Gets the path of the specified package. (GetPackagePathByFullName)
helpviewer_keywords: ["GetPackagePathByFullName","GetPackagePathByFullName function [App packaging and management]","appmodel/GetPackagePathByFullName","appxpkg.getpackagepathbyfullname"]
old-location: appxpkg\getpackagepathbyfullname.htm
tech.root: appxpkg
ms.assetid: 9C25708C-1464-4C59-9740-E9F105116385
ms.date: 12/05/2018
ms.keywords: GetPackagePathByFullName, GetPackagePathByFullName function [App packaging and management], appmodel/GetPackagePathByFullName, appxpkg.getpackagepathbyfullname
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
 - GetPackagePathByFullName
 - appmodel/GetPackagePathByFullName
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
 - GetPackagePathByFullName
---

# GetPackagePathByFullName function


## -description

Gets the path of the specified package.

## -parameters

### -param packageFullName [in]

Type: <b>PCWSTR</b>

The full name of the package.

### -param pathLength [in, out]

Type: <b>UINT32*</b>

A pointer to a variable that holds the number of characters (<b>WCHAR</b>s) in the package path string, which includes the null-terminator. 

First you pass <b>NULL</b> to <i>path</i> to get the number of characters. You use this number to allocate memory space for <i>path</i>. Then you pass the address of this memory space to fill <i>path</i>.

### -param path [out, optional]

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

## -see-also

[GetPackagePathByFullName2](nf-appmodel-getpackagepathbyfullname2.md)

