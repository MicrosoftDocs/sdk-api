---
UID: NF:wslapi.WslGetDistributionConfiguration
title: WslGetDistributionConfiguration function (wslapi.h)
description: Retrieves the current configuration of a distribution registered with the Windows Subsystem for Linux (WSL).
helpviewer_keywords: ["WslGetDistributionConfiguration","WslGetDistributionConfiguration function","wsl.wslgetdistributionconfiguration","wslapi/WslGetDistributionConfiguration"]
old-location: wsl\wslgetdistributionconfiguration.htm
tech.root: wsl
ms.assetid: 7D680D81-921E-461F-8845-AADAF53EAEEE
ms.date: 12/05/2018
ms.keywords: WslGetDistributionConfiguration, WslGetDistributionConfiguration function, wsl.wslgetdistributionconfiguration, wslapi/WslGetDistributionConfiguration
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
 - WslGetDistributionConfiguration
 - wslapi/WslGetDistributionConfiguration
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
 - WslGetDistributionConfiguration
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

