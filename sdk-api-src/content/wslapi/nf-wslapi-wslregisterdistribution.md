---
UID: NF:wslapi.WslRegisterDistribution
title: WslRegisterDistribution function
author: windows-sdk-content
description: Registers a new distribution with the Windows Subsystem for Linux (WSL).
old-location: wsl\wslregisterdistribution.htm
old-project: wsl
ms.assetid: 34D5D38D-A155-42DE-9E9B-2BD7E414E4EC
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WslRegisterDistribution, WslRegisterDistribution function, wsl.wslregisterdistribution, wslapi/WslRegisterDistribution
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wslapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: WSL_DISTRIBUTION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-wsl-api-l1-1-0.dll
api_name:
 - WslRegisterDistribution
product: Windows
targetos: Windows
req.lib: Wslapi.lib
req.dll: Api-ms-win-wsl-api-l1-1-0.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WslRegisterDistribution function


## -description


Registers a new distribution with the Windows Subsystem for Linux (WSL).


## -parameters




### -param distributionName [in]

Unique name representing a distribution (for example, "Fabrikam.Distro.10.01").


### -param tarGzFilename [in]

Full path to a .tar.gz file containing the file system of the distribution to register.


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
 



