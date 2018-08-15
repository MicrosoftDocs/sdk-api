---
UID: NF:wslapi.WslUnregisterDistribution
title: WslUnregisterDistribution function
author: windows-sdk-content
description: Unregisters a distribution from the Windows Subsystem for Linux (WSL).
old-location: wsl\wslunregisterdistribution.htm
old-project: wsl
ms.assetid: B655E05D-4F4E-401D-8A24-6E8E8B0CE00C
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WslUnregisterDistribution, WslUnregisterDistribution function, wsl.wslunregisterdistribution, wslapi/WslUnregisterDistribution
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
 - WslUnregisterDistribution
product: Windows
targetos: Windows
req.lib: Wslapi.lib
req.dll: Api-ms-win-wsl-api-l1-1-0.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WslUnregisterDistribution function


## -description


Unregisters a distribution from the Windows Subsystem for Linux (WSL).


## -parameters




### -param distributionName [in]

Unique name representing a distribution (for example, "Fabrikam.Distro.10.01").


## -returns



Returns S_OK on success, or a failing HRESULT otherwise.



