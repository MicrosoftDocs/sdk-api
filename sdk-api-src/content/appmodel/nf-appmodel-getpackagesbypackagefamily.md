---
UID: NF:appmodel.GetPackagesByPackageFamily
title: GetPackagesByPackageFamily function
author: windows-sdk-content
description: Gets the packages with the specified family name for the current user.
old-location: appxpkg\getpackagesbypackagefamily.htm
old-project: appxpkg
ms.assetid: C2163203-D654-4491-9090-0CC43F42EC35
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: GetPackagesByPackageFamily, GetPackagesByPackageFamily function [App packaging and management], appmodel/GetPackagesByPackageFamily, appxpkg.getpackagesbypackagefamily
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
 - Ext-MS-Win-kernel32-package-l1-1-0.dll
 - Kernel.AppCore.dll
 - API-MS-Win-AppModel-RunTime-l1-1-1.dll
 - Ext-MS-Win-Kernel32-package-l1-1-2.dll
 - ext-ms-win-kernel32-package-l1-1-1.dll
 - API-MS-Win-AppModel-Runtime-L1-1-2.dll
api_name:
 - GetPackagesByPackageFamily
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
---

# GetPackagesByPackageFamily function


## -description


Gets the packages  with the specified family name for the current user.




## -parameters




### -param packageFamilyName [in]

Type: <b>PCWSTR</b>

The package family name.


### -param count [in, out]

Type: <b>UINT32*</b>

A pointer to a variable that holds the number of package full names. 

First you pass <b>NULL</b> to <i>packageFullNames</i> to get the number of package full names. You use this number to allocate memory space for <i>packageFullNames</i>. Then you pass the address of this number to fill <i>packageFullNames</i>.


### -param packageFullNames [out, optional]

Type: <b>PWSTR*</b>

A pointer to the strings of package full names.


### -param bufferLength [in, out]

Type: <b>UINT32*</b>

A pointer to a variable that holds the number of characters in the string of package full names. 

First you pass <b>NULL</b> to <i>buffer</i> to get the number of characters. You use this number to allocate memory space for <i>buffer</i>. Then you pass the address of this number to fill <i>buffer</i>.


### -param buffer [out, optional]

Type: <b>WCHAR*</b>

The string of characters for all of the package full names.


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
One or more buffer is not large enough to hold the data. The required size is specified  by either <i>count</i> or <i>buffer</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4AA5BD75-F865-40D6-9C10-E54C197D47C4">PackageNameAndPublisherIdFromFamilyName</a>
 

 

