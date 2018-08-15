---
UID: NF:comsvcs.IServiceSxsConfig.SxsDirectory
title: IServiceSxsConfig::SxsDirectory
author: windows-sdk-content
description: Sets the directory for the side-by-side assembly for the enclosed work.
old-location: cos\iservicesxsconfig_sxsdirectory.htm
old-project: cossdk
ms.assetid: 5eb909a5-7730-4f0b-aee6-9bb8de076cea
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IServiceSxsConfig interface [COM+],SxsDirectory method, IServiceSxsConfig.SxsDirectory, IServiceSxsConfig::SxsDirectory, SxsDirectory, SxsDirectory method [COM+], SxsDirectory method [COM+],IServiceSxsConfig interface, _cos_IServiceSxsConfig_SxsDirectory, comsvcs/IServiceSxsConfig::SxsDirectory, cos.iservicesxsconfig_sxsdirectory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServiceSxsConfig.SxsDirectory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceSxsConfig::SxsDirectory


## -description


Sets the directory for the side-by-side assembly for the enclosed work.


## -parameters




### -param szSxsDirectory [in]

The name of the directory for the side-by-side assembly that is to be used for the enclosed work.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



This method must be called if a new side-by-side assembly domain is created using the call to <a href="https://msdn.microsoft.com/ce067aca-8bb4-48ac-b466-9080d2166bdd">SxsConfig</a>.





## -see-also




<a href="https://msdn.microsoft.com/24d4a22b-0a01-4bf2-9cc6-4a1b31897d05">IServiceSxsConfig</a>
 

 

