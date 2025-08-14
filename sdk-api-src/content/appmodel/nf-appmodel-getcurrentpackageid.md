---
UID: NF:appmodel.GetCurrentPackageId
title: GetCurrentPackageId function (appmodel.h)
description: Gets the package identifier (ID) for the calling process.
helpviewer_keywords: ["GetCurrentPackageId","GetCurrentPackageId function [App packaging and management]","appmodel/GetCurrentPackageId","appxpkg.getcurrentpackageid"]
old-location: appxpkg\getcurrentpackageid.htm
tech.root: appxpkg
ms.assetid: 4CFC707A-2A5A-41FE-BB5F-6FECACC99271
ms.date: 12/05/2018
ms.keywords: GetCurrentPackageId, GetCurrentPackageId function [App packaging and management], appmodel/GetCurrentPackageId, appxpkg.getcurrentpackageid
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
 - GetCurrentPackageId
 - appmodel/GetCurrentPackageId
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
 - Ext-MS-Win-kernel32-package-current-l1-1-0.dll
 - modernapiexthost.dll
 - kernel.appcore.dll
 - API-MS-Win-AppModel-Runtime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - GetCurrentPackageId
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

<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackagefamilyname">GetCurrentPackageFamilyName</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackagefullname">GetCurrentPackageFullName</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackageinfo">GetCurrentPackageInfo</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getcurrentpackagepath">GetCurrentPackagePath</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-getpackageid">GetPackageId</a>



<a href="/windows/desktop/api/appmodel/nf-appmodel-packageidfromfullname">PackageIdFromFullName</a>