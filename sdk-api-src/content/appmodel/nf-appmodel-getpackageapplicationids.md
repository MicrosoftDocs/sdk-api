---
UID: NF:appmodel.GetPackageApplicationIds
title: GetPackageApplicationIds function (appmodel.h)
description: Gets the IDs of apps in the specified package.
helpviewer_keywords: ["GetPackageApplicationIds","GetPackageApplicationIds function [App packaging and management]","appmodel/GetPackageApplicationIds","appxpkg.getpackageapplicationids"]
old-location: appxpkg\getpackageapplicationids.htm
tech.root: appxpkg
ms.assetid: F08135F9-FF45-4309-84B5-77F4AFD7FC0C
ms.date: 12/05/2018
ms.keywords: GetPackageApplicationIds, GetPackageApplicationIds function [App packaging and management], appmodel/GetPackageApplicationIds, appxpkg.getpackageapplicationids
req.header: appmodel.h
req.include-header: 
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetPackageApplicationIds
 - appmodel/GetPackageApplicationIds
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
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - Kernel.AppCore.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - GetPackageApplicationIds
---

# GetPackageApplicationIds function


## -description

Gets the IDs of apps in the specified package.

## -parameters

### -param packageInfoReference [in]

Type: <b>PACKAGE_INFO_REFERENCE</b>

A reference to package information.

### -param bufferLength [in, out]

Type: <b>UINT32*</b>

A pointer to a variable that holds the size of <i>buffer</i>, in bytes. 

First you pass <b>NULL</b> to <i>buffer</i> to get the required size of <i>buffer</i>. You use this number to allocate memory space for <i>buffer</i>. Then you pass the address of this memory space to fill <i>buffer</i>.

### -param buffer [out, optional]

Type: <b>BYTE*</b>

A pointer to memory space that receives  the app IDs.

### -param count [out, optional]

Type: <b>UINT32*</b>

A pointer to a variable that receives the number of app IDs in <i>buffer</i>.

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

