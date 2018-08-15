---
UID: NF:appmodel.GetStagedPackageOrigin
title: GetStagedPackageOrigin function
author: windows-sdk-content
description: Gets the origin of the specified package.
old-location: appxpkg\getstagedpackageorigin.htm
old-project: appxpkg
ms.assetid: 7A1EE2CA-83CE-4E03-85A5-0061E29EB49B
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetStagedPackageOrigin, GetStagedPackageOrigin function [App packaging and management], appmodel/GetStagedPackageOrigin, appxpkg.getstagedpackageorigin
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: appmodel.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PackageOrigin
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - Kernel.AppCore.dll
 - Ext-MS-Win-Kernel32-package-l1-1-2.dll
 - ext-ms-win-kernel32-package-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - GetStagedPackageOrigin
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
---

# GetStagedPackageOrigin function


## -description


Gets the origin of the specified package.


## -parameters




### -param packageFullName [in]

Type: <b>PCWSTR</b>

The full name of the package.


### -param origin [out]

Type: <b><a href="https://msdn.microsoft.com/0CB9CE97-8A54-4BE7-B054-00F29D36CAB2">PackageOrigin</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/0CB9CE97-8A54-4BE7-B054-00F29D36CAB2">PackageOrigin</a>-typed value that indicates the origin of the package specified by <i>packageFullName</i>.


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
 



