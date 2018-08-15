---
UID: NF:appmodel.GetCurrentPackagePath
title: GetCurrentPackagePath function
author: windows-sdk-content
description: Gets the package path for the calling process.
old-location: appxpkg\getcurrentpackagepath.htm
old-project: appxpkg
ms.assetid: 46CE81DF-A9D5-492E-AB5E-4F043DC326E2
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetCurrentPackagePath, GetCurrentPackagePath function [App packaging and management], appmodel/GetCurrentPackagePath, appxpkg.getcurrentpackagepath
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
 - Kernel.AppCore.dll
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - GetCurrentPackagePath
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
---

# GetCurrentPackagePath function


## -description


Gets the package path for the calling process.


## -parameters




### -param pathLength [in, out]

Type: <b>UINT32*</b>

On input, the size of the <i>path</i> buffer, in characters. On output, the size of the package path returned, in characters, including the null terminator.


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
<dt><b>APPMODEL_ERROR_NO_PACKAGE</b></dt>
</dl>
</td>
<td width="60%">
The process has no package identity.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to hold the data. The required size is specified  by <i>pathLength</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/39DBFBDD-A1CC-45C3-A5DD-5ED9697F9AFE">GetCurrentPackageFamilyName</a>



<a href="https://msdn.microsoft.com/D5B00C53-1FBF-4245-92D1-FA39713A9EE7">GetCurrentPackageFullName</a>



<a href="https://msdn.microsoft.com/4CFC707A-2A5A-41FE-BB5F-6FECACC99271">GetCurrentPackageId</a>



<a href="https://msdn.microsoft.com/A1887D61-0FAD-4BE8-850F-F104CC074798">GetCurrentPackageInfo</a>



<a href="https://msdn.microsoft.com/BDA0DD87-A36D-486B-BF89-EA5CC105C742">GetPackagePath</a>
 

 

