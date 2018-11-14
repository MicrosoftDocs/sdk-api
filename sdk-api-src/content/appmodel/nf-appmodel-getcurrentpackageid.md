---
UID: NF:appmodel.GetCurrentPackageId
title: GetCurrentPackageId function
author: windows-sdk-content
description: Gets the package identifier (ID) for the calling process.
old-location: appxpkg\getcurrentpackageid.htm
tech.root: appxpkg
ms.assetid: 4CFC707A-2A5A-41FE-BB5F-6FECACC99271
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetCurrentPackageId, GetCurrentPackageId function [App packaging and management], appmodel/GetCurrentPackageId, appxpkg.getcurrentpackageid
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
 - Ext-MS-Win-kernel32-package-current-l1-1-0.dll
 - modernapiexthost.dll
 - kernel.appcore.dll
 - API-MS-Win-AppModel-Runtime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - GetCurrentPackageId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetCurrentPackageId
: 
---

# GetCurrentPackageId function


## -description


Gets the package identifier (ID) for the calling process.


## -parameters




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




<a href="https://msdn.microsoft.com/39DBFBDD-A1CC-45C3-A5DD-5ED9697F9AFE">GetCurrentPackageFamilyName</a>



<a href="https://msdn.microsoft.com/D5B00C53-1FBF-4245-92D1-FA39713A9EE7">GetCurrentPackageFullName</a>



<a href="https://msdn.microsoft.com/A1887D61-0FAD-4BE8-850F-F104CC074798">GetCurrentPackageInfo</a>



<a href="https://msdn.microsoft.com/46CE81DF-A9D5-492E-AB5E-4F043DC326E2">GetCurrentPackagePath</a>



<a href="https://msdn.microsoft.com/BA5D87F5-72FD-48BE-A104-EC7D1459FD58">GetPackageId</a>



<a href="https://msdn.microsoft.com/EED832F8-E4F7-4A0F-93E2-451F78F67767">PackageIdFromFullName</a>
 

 

