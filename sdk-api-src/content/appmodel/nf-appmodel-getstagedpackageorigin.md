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

# GetStagedPackageOrigin function


## -description


Gets the origin of the specified package.


## -parameters




### -param packageFullName [in]

Type: <b>PCWSTR</b>

The full name of the package.


### -param origin [out]

Type: <b><a href="https://msdn.microsoft.com/0CB9CE97-8A54-4BE7-B054-00F29D36CAB2">PackageOrigin</a>*</b>

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/0CB9CE97-8A54-4BE7-B054-00F29D36CAB2">PackageOrigin</a>-typed value that indicates the origin of the package specified by <i>packageFullName</i>.


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>packageFullName</i> parameter isn't valid.

</td>
</tr>
</table>
 



