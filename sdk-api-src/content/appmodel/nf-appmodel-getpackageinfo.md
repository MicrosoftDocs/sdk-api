---
UID: NF:appmodel.GetPackageInfo
title: GetPackageInfo function
author: windows-sdk-content
description: Gets the package information for the specified package.
old-location: appxpkg\getpackageinfo.htm
tech.root: appxpkg
ms.assetid: 28F45B3B-A61F-44D3-B606-6966AD5866FA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPackageInfo, GetPackageInfo function [App packaging and management], appmodel/GetPackageInfo, appxpkg.getpackageinfo
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
 - GetPackageInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

The <a href="https://msdn.microsoft.com/72E565C3-6CFD-47E3-8BAC-17D6E86B99DA">package constants</a> that specify how package information is retrieved.


### -param bufferLength [in, out]

Type: <b>UINT32*</b>

On input, the size of <i>buffer</i>, in bytes. On output, the size of the package information returned, in bytes.


### -param buffer [out, optional]

Type: <b>BYTE*</b>

The package information, represented as an array of <a href="https://msdn.microsoft.com/0DDE00D1-9C5F-4F2B-8110-A92B1FFA1B64">PACKAGE_INFO</a> structures.


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




<a href="https://msdn.microsoft.com/BA84FB47-F241-4120-9441-7E1149F68738">ClosePackageInfo</a>



<a href="https://msdn.microsoft.com/A1887D61-0FAD-4BE8-850F-F104CC074798">GetCurrentPackageInfo</a>



<a href="https://msdn.microsoft.com/BDA0DD87-A36D-486B-BF89-EA5CC105C742">GetPackagePath</a>



<a href="https://msdn.microsoft.com/9ECFC757-1CB3-43A1-BA45-9AF72CAB240E">OpenPackageInfoByFullName</a>
 

 

