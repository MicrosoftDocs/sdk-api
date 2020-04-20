---
UID: NF:appmodel.OpenPackageInfoByFullName
title: OpenPackageInfoByFullName function (appmodel.h)
description: Opens the package information of the specified package.helpviewer_keywords: ["OpenPackageInfoByFullName","OpenPackageInfoByFullName function [App packaging and management]","appmodel/OpenPackageInfoByFullName","appxpkg.openpackageinfobyfullname"]
old-location: appxpkg\openpackageinfobyfullname.htm
tech.root: appxpkg
ms.assetid: 9ECFC757-1CB3-43A1-BA45-9AF72CAB240E
ms.date: 12/05/2018
ms.keywords: OpenPackageInfoByFullName, OpenPackageInfoByFullName function [App packaging and management], appmodel/OpenPackageInfoByFullName, appxpkg.openpackageinfobyfullname
f1_keywords:
- appmodel/OpenPackageInfoByFullName
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-closepackageinfo">ClosePackageInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appmodel/nf-appmodel-getpackageinfo">GetPackageInfo</a>
 

 

