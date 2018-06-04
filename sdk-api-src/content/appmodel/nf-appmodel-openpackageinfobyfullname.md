---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# OpenPackageInfoByFullName function


## -description


Opens the package information of the specified package.


## -parameters




### -param packageFullName [in]

Type: <b>PCWSTR</b>

The full name of the package.


### -param reserved

Type: <b>const UINT32</b>

Reserved; must be 0.


### -param packageInfoReference [out]

Type: <b>PACKAGE_INFO_REFERENCE*</b>

A reference to package information.


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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The package is not installed for the current user.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/BA84FB47-F241-4120-9441-7E1149F68738">ClosePackageInfo</a>



<a href="https://msdn.microsoft.com/28F45B3B-A61F-44D3-B606-6966AD5866FA">GetPackageInfo</a>
 

 

