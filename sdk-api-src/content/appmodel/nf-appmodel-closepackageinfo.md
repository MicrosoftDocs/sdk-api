---
UID: NF:appmodel.ClosePackageInfo
title: ClosePackageInfo function (appmodel.h)
author: windows-sdk-content
description: Closes a reference to the specified package information.
old-location: appxpkg\closepackageinfo.htm
tech.root: appxpkg
ms.assetid: BA84FB47-F241-4120-9441-7E1149F68738
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClosePackageInfo, ClosePackageInfo function [App packaging and management], appmodel/ClosePackageInfo, appxpkg.closepackageinfo
ms.topic: function
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
 - ClosePackageInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
 

 

