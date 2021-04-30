---
UID: NF:wslapi.WslUnregisterDistribution
title: WslUnregisterDistribution function (wslapi.h)
description: Unregisters a distribution from the Windows Subsystem for Linux (WSL).
helpviewer_keywords: ["WslUnregisterDistribution","WslUnregisterDistribution function","wsl.wslunregisterdistribution","wslapi/WslUnregisterDistribution"]
old-location: wsl\wslunregisterdistribution.htm
tech.root: wsl
ms.assetid: B655E05D-4F4E-401D-8A24-6E8E8B0CE00C
ms.date: 12/05/2018
ms.keywords: WslUnregisterDistribution, WslUnregisterDistribution function, wsl.wslunregisterdistribution, wslapi/WslUnregisterDistribution
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
 - WslUnregisterDistribution
 - wslapi/WslUnregisterDistribution
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
 - WslUnregisterDistribution
---

# WslUnregisterDistribution function


## -description

Unregisters a distribution from the Windows Subsystem for Linux (WSL).

## -parameters

### -param distributionName [in]

Unique name representing a distribution (for example, "Fabrikam.Distro.10.01").

## -returns

Returns S_OK on success, or a failing HRESULT otherwise.

