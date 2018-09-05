---
UID: NF:wslapi.WslGetDistributionConfiguration
title: WslGetDistributionConfiguration function
author: windows-sdk-content
description: Retrieves the current configuration of a distribution registered with the Windows Subsystem for Linux (WSL).
old-location: wsl\wslgetdistributionconfiguration.htm
old-project: wsl
ms.assetid: 7D680D81-921E-461F-8845-AADAF53EAEEE
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WslGetDistributionConfiguration, WslGetDistributionConfiguration function, wsl.wslgetdistributionconfiguration, wslapi/WslGetDistributionConfiguration
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
 - WslGetDistributionConfiguration
product: Windows
targetos: Windows
req.lib: Wslapi.lib
req.dll: Api-ms-win-wsl-api-l1-1-0.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WslGetDistributionConfiguration function


## -description


   Retrieves the current configuration of a distribution registered with the Windows Subsystem for Linux (WSL).


## -parameters




### -param distributionName [in]

Unique name representing a distribution (for example, "Fabrikam.Distro.10.01").


### -param distributionVersion [out]

The version of WSL for which this distribution is configured.


### -param defaultUID [out]

The default user ID used when launching new WSL sessions for this distribution.


### -param wslDistributionFlags [out]

The flags governing the behavior of this distribution.


### -param defaultEnvironmentVariables [out]

The address of a pointer to an array of default environment variable strings used when launching new WSL sessions for this distribution.


### -param defaultEnvironmentVariableCount [out]

The number of elements in <i>pDefaultEnvironmentVariablesArray</i>.


## -returns



Returns S_OK on success, or a failing HRESULT otherwise.




## -remarks



The caller is responsible for freeing each string in <i>pDefaultEnvironmentVariablesArray</i> (and the array itself) via <b>CoTaskMemFree</b>.



