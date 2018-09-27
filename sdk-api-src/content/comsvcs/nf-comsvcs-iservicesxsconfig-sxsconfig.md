---
UID: NF:comsvcs.IServiceSxsConfig.SxsConfig
title: IServiceSxsConfig::SxsConfig
author: windows-sdk-content
description: Configures the side-by-side assembly for the enclosed work.
old-location: cos\iservicesxsconfig_sxsconfig.htm
tech.root: cossdk
ms.assetid: ce067aca-8bb4-48ac-b466-9080d2166bdd
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IServiceSxsConfig interface [COM+],SxsConfig method, IServiceSxsConfig.SxsConfig, IServiceSxsConfig::SxsConfig, SxsConfig, SxsConfig method [COM+], SxsConfig method [COM+],IServiceSxsConfig interface, _cos_IServiceSxsConfig_SxsConfig, comsvcs/IServiceSxsConfig::SxsConfig, cos.iservicesxsconfig_sxsconfig
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServiceSxsConfig.SxsConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServiceSxsConfig::SxsConfig


## -description


Configures the side-by-side assembly for the enclosed work.


## -parameters




### -param scsConfig [in]

A value from the <a href="https://msdn.microsoft.com/8c114e9e-b201-4317-8a45-d5b0964c6ff8">CSC_SxsConfig</a> enumeration.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



The <a href="https://msdn.microsoft.com/5eb909a5-7730-4f0b-aee6-9bb8de076cea">SxsDirectory</a> method must be called if a new side-by-side assembly domain is created using a call to this method.





## -see-also




<a href="https://msdn.microsoft.com/24d4a22b-0a01-4bf2-9cc6-4a1b31897d05">IServiceSxsConfig</a>
 

 

