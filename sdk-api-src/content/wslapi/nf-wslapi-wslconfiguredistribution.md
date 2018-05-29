---
UID: NF:wslapi.WslConfigureDistribution
title: WslConfigureDistribution function
author: windows-sdk-content
description: Modifies the behavior of a distribution registered with the Windows Subsystem for Linux (WSL).
old-location: wsl\wslconfiguredistribution.htm
old-project: wsl
ms.assetid: 4E89F367-4E10-4E76-93BC-FD5E2450D430
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: WslConfigureDistribution, WslConfigureDistribution function, wsl.wslconfiguredistribution, wslapi/WslConfigureDistribution
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: WSL_DISTRIBUTION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	api-ms-win-wsl-api-l1-1-0.dll
api_name:
-	WslConfigureDistribution
product: Windows
targetos: Windows
req.lib: Wslapi.lib
req.dll: Api-ms-win-wsl-api-l1-1-0.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WslConfigureDistribution function


## -description


Modifies the behavior of a distribution registered with the Windows Subsystem for Linux (WSL).


## -parameters




### -param distributionName

TBD


### -param defaultUID

The Linux user ID to use when launching new WSL sessions for this distribution.


### -param wslDistributionFlags

TBD




#### - distroName

Unique name representing a distribution (for example, "Fabrikam.Distro.10.01").


#### - wslFlags

Flags specifying what behavior to use for this distribution.


## -returns



Returns S_OK on success, or a failing HRESULT otherwise.



