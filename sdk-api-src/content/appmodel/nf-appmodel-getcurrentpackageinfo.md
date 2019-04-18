---
UID: NF:appmodel.GetCurrentPackageInfo
title: GetCurrentPackageInfo function (appmodel.h)
author: windows-sdk-content
description: Gets the package information for the calling process.
old-location: appxpkg\getcurrentpackageinfo.htm
tech.root: appxpkg
ms.assetid: A1887D61-0FAD-4BE8-850F-F104CC074798
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCurrentPackageInfo, GetCurrentPackageInfo function [App packaging and management], appmodel/GetCurrentPackageInfo, appxpkg.getcurrentpackageinfo
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
 - Ext-MS-Win-kernel32-package-current-l1-1-0.dll
 - modernapiexthost.dll
 - kernel.appcore.dll
 - API-MS-Win-AppModel-Runtime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - GetCurrentPackageInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCurrentPackageInfo function


## -description


Gets the package information for the calling process.


## -parameters




### -param flags [in]

Type: <b>const UINT32</b>

The <a href="https://msdn.microsoft.com/72E565C3-6CFD-47E3-8BAC-17D6E86B99DA">package constants</a> that specify how package information is retrieved. The <b>PACKAGE_FILTER_*</b> flags are supported.


### -param bufferLength [in, out]

Type: <b>UINT32*</b>

On input, the size of <i>buffer</i>, in bytes. On output, the size of the array of structures returned, in bytes.


### -param buffer [out, optional]

Type: <b>BYTE*</b>

The package information, represented as an array of <a href="https://msdn.microsoft.com/0DDE00D1-9C5F-4F2B-8110-A92B1FFA1B64">PACKAGE_INFO</a> structures.


### -param count [out, optional]

Type: <b>UINT32*</b>

The number of structures in the buffer.


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
The buffer is not large enough to hold the data. The required size is specified  by <i>bufferLength</i>.

</td>
</tr>
</table>
 




## -see-also


[GetCurrentPackageInfo2](nf-appmodel-getcurrentpackageinfo2.md)



<a href="https://msdn.microsoft.com/39DBFBDD-A1CC-45C3-A5DD-5ED9697F9AFE">GetCurrentPackageFamilyName</a>



<a href="https://msdn.microsoft.com/D5B00C53-1FBF-4245-92D1-FA39713A9EE7">GetCurrentPackageFullName</a>



<a href="https://msdn.microsoft.com/4CFC707A-2A5A-41FE-BB5F-6FECACC99271">GetCurrentPackageId</a>



<a href="https://msdn.microsoft.com/46CE81DF-A9D5-492E-AB5E-4F043DC326E2">GetCurrentPackagePath</a>



<a href="https://msdn.microsoft.com/28F45B3B-A61F-44D3-B606-6966AD5866FA">GetPackageInfo</a>
 

 

