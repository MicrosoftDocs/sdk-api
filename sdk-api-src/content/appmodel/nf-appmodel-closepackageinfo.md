---
UID: NF:appmodel.ClosePackageInfo
title: ClosePackageInfo function
author: windows-sdk-content
description: Closes a reference to the specified package information.
old-location: appxpkg\closepackageinfo.htm
old-project: appxpkg
ms.assetid: BA84FB47-F241-4120-9441-7E1149F68738
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ClosePackageInfo, ClosePackageInfo function [App packaging and management], appmodel/ClosePackageInfo, appxpkg.closepackageinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: appmodel.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PackageOrigin
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
 - ClosePackageInfo
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
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




<a href="https://msdn.microsoft.com/9ECFC757-1CB3-43A1-BA45-9AF72CAB240E">OpenPackageInfoByFullName</a>
 

 

