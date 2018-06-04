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

# WslRegisterDistribution function


## -description


Registers a new distribution with the Windows Subsystem for Linux (WSL).


## -parameters




### -param distributionName

TBD


### -param tarGzFilename [in]

Full path to a .tar.gz file containing the file system of the distribution to register.


#### - distroName [in]

Unique name representing a distribution (for example, "Fabrikam.Distro.10.01").


## -returns



This function can return one of the following values. Use the SUCCEEDED and FAILED macros to test the return value of this function.

<table>
<tr>
<td><b>Return Code</b></td>
<td><b>Description</b></td>
</tr>
<tr>
<td>S_OK                                     </td>
<td>Distribution successfully registered with the Windows Subsystem for Linux.</td>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS) </td>
<td>Failed because a distribution with this name has already been registered.</td>
</tr>
</table>
 



