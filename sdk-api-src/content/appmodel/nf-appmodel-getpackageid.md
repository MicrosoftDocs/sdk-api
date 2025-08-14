---
UID: NF:appmodel.GetPackageId
title: GetPackageId function (appmodel.h)
description: Gets the package identifier (ID) for the specified process.
helpviewer_keywords: ["GetPackageId","GetPackageId function [App packaging and management]","appmodel/GetPackageId","appxpkg.getpackageid"]
old-location: appxpkg\getpackageid.htm
tech.root: appxpkg
ms.assetid: BA5D87F5-72FD-48BE-A104-EC7D1459FD58
ms.date: 12/05/2018
ms.keywords: GetPackageId, GetPackageId function [App packaging and management], appmodel/GetPackageId, appxpkg.getpackageid
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
 - GetPackageId
 - appmodel/GetPackageId
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
 - GetPackageId
---

# GetPackageId function


## -description

Gets the package identifier (ID) for the specified process.

## -parameters

### -param hProcess [in]

Type: <b>HANDLE</b>

A handle to the process that has the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param bufferLength [in, out]

Type: <b>UINT32*</b>

On input, the size of <i>buffer</i>, in bytes. On output, the size of the structure returned, in bytes.

### -param buffer [out, optional]

Type: <b>BYTE*</b>

The package ID, represented as a <a href="/windows/desktop/api/appmodel/ns-appmodel-package_id">PACKAGE_ID</a> structure.

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

<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackageid">GetCurrentPackageId</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getpackagefamilyname">GetPackageFamilyName</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getpackagefullname">GetPackageFullName</a>