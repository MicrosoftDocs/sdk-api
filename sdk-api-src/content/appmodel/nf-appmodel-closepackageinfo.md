---
UID: NF:appmodel.ClosePackageInfo
title: ClosePackageInfo function (appmodel.h)
description: Closes a reference to the specified package information.
helpviewer_keywords: ["ClosePackageInfo","ClosePackageInfo function [App packaging and management]","appmodel/ClosePackageInfo","appxpkg.closepackageinfo"]
old-location: appxpkg\closepackageinfo.htm
tech.root: appxpkg
ms.assetid: BA84FB47-F241-4120-9441-7E1149F68738
ms.date: 12/05/2018
ms.keywords: ClosePackageInfo, ClosePackageInfo function [App packaging and management], appmodel/ClosePackageInfo, appxpkg.closepackageinfo
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
 - ClosePackageInfo
 - appmodel/ClosePackageInfo
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
 - ClosePackageInfo
---

# ClosePackageInfo function


## -description

Closes a reference to the specified package information.

## -parameters

### -param packageInfoReference [in]

Type: <b>PACKAGE_INFO_REFERENCE</b>

A reference to package information.

## -returns

Type: <b>LONG</b>

If the function succeeds it returns <b>ERROR_SUCCESS</b>. Otherwise, the function returns an error code.

## -see-also

<a href="/windows/desktop/api/appmodel/nf-appmodel-openpackageinfobyfullname">OpenPackageInfoByFullName</a>