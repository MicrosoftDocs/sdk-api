---
UID: NF:wslapi.WslRegisterDistribution
title: WslRegisterDistribution function (wslapi.h)
description: Registers a new distribution with the Windows Subsystem for Linux (WSL).
helpviewer_keywords: ["WslRegisterDistribution","WslRegisterDistribution function","wsl.wslregisterdistribution","wslapi/WslRegisterDistribution"]
old-location: wsl\wslregisterdistribution.htm
tech.root: wsl
ms.assetid: 34D5D38D-A155-42DE-9E9B-2BD7E414E4EC
ms.date: 12/05/2018
ms.keywords: WslRegisterDistribution, WslRegisterDistribution function, wsl.wslregisterdistribution, wslapi/WslRegisterDistribution
req.header: wslapi.h
req.include-header: 
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
req.lib: Wslapi.lib
req.dll: Api-ms-win-wsl-api-l1-1-0.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WslRegisterDistribution
 - wslapi/WslRegisterDistribution
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-wsl-api-l1-1-0.dll
api_name:
 - WslRegisterDistribution
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

