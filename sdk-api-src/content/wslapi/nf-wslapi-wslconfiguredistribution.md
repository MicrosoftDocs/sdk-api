---
UID: NF:wslapi.WslConfigureDistribution
title: WslConfigureDistribution function (wslapi.h)
description: Modifies the behavior of a distribution registered with the Windows Subsystem for Linux (WSL).
helpviewer_keywords: ["WslConfigureDistribution","WslConfigureDistribution function","wsl.wslconfiguredistribution","wslapi/WslConfigureDistribution"]
old-location: wsl\wslconfiguredistribution.htm
tech.root: wsl
ms.assetid: 4E89F367-4E10-4E76-93BC-FD5E2450D430
ms.date: 12/05/2018
ms.keywords: WslConfigureDistribution, WslConfigureDistribution function, wsl.wslconfiguredistribution, wslapi/WslConfigureDistribution
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
 - WslConfigureDistribution
 - wslapi/WslConfigureDistribution
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
 - WslConfigureDistribution
---

# WslConfigureDistribution function


## -description

Modifies the behavior of a distribution registered with the Windows Subsystem for Linux (WSL).

## -parameters

### -param distributionName

Unique name representing a distribution (for example, "Fabrikam.Distro.10.01").

### -param defaultUID

The Linux user ID to use when launching new WSL sessions for this distribution.

### -param wslDistributionFlags

Flags specifying what behavior to use for this distribution.

## -returns

Returns S_OK on success, or a failing HRESULT otherwise.

