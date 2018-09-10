---
UID: NF:appmodel.GetPackageId
title: GetPackageId function
author: windows-sdk-content
description: Gets the package identifier (ID) for the specified process.
old-location: appxpkg\getpackageid.htm
tech.root: appxpkg
ms.assetid: BA5D87F5-72FD-48BE-A104-EC7D1459FD58
ms.author: windowssdkdev
ms.date: 08/16/2018
ms.keywords: GetPackageId, GetPackageId function [App packaging and management], appmodel/GetPackageId, appxpkg.getpackageid
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - GetPackageId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPackageId function


## -description


Gets the package identifier (ID) for the specified process.


## -parameters




### -param hProcess [in]

Type: <b>HANDLE</b>

A handle to the process that has the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param bufferLength [in, out]

Type: <b>UINT32*</b>

On input, the size of <i>buffer</i>, in bytes. On output, the size of the structure returned, in bytes.


### -param buffer [out, optional]

Type: <b>BYTE*</b>

The package ID, represented as a <a href="https://msdn.microsoft.com/4B15281A-2227-47B7-A750-0A01DB8543FC">PACKAGE_ID</a> structure.


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




<a href="https://msdn.microsoft.com/4CFC707A-2A5A-41FE-BB5F-6FECACC99271">GetCurrentPackageId</a>



<a href="https://msdn.microsoft.com/AC239898-9924-4193-9072-7A7EEC2D03E9">GetPackageFamilyName</a>



<a href="https://msdn.microsoft.com/D1BA8E91-A3D1-454A-A4F6-E3C786F0BD7E">GetPackageFullName</a>
 

 

