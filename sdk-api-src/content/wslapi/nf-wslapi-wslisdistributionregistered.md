---
UID: NF:wslapi.WslIsDistributionRegistered
title: WslIsDistributionRegistered function (wslapi.h)
author: windows-sdk-content
description: Determines if a distribution is registered with the Windows Subsystem for Linux (WSL).
old-location: wsl\wslisdistributionregistered.htm
tech.root: wsl
ms.assetid: 51751073-922D-43B9-A253-2017CEEC262A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WslIsDistributionRegistered, WslIsDistributionRegistered function, wsl.wslisdistributionregistered, wslapi/WslIsDistributionRegistered
ms.topic: function
f1_keywords: 
 - "wslapi/WslIsDistributionRegistered"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-wsl-api-l1-1-0.dll
api_name:
 - WslIsDistributionRegistered
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WslIsDistributionRegistered function


## -description


Determines if a distribution is registered with the Windows Subsystem for Linux (WSL).


## -parameters




### -param distributionName

Unique name representing a distribution (for example, "Fabrikam.Distro.10.01").


## -returns



Returns TRUE if the supplied distribution is currently registered, or FALSE otherwise.



