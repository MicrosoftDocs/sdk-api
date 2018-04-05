---
UID: NF:comsvcs.IAssemblyLocator.GetModules
title: IAssemblyLocator::GetModules method
author: windows-driver-content
description: Used to get the names of the modules that are contained in an assembly.
old-location: cos\iassemblylocator_getmodules.htm
old-project: cossdk
ms.assetid: 5483c500-ac11-4f1d-b89c-37b6a718a735
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetModules method [COM+], GetModules method [COM+], IAssemblyLocator interface, GetModules,IAssemblyLocator.GetModules, IAssemblyLocator, IAssemblyLocator interface [COM+], GetModules method, IAssemblyLocator::GetModules, _cos_IAssemblyLocator_GetModules, comsvcs/IAssemblyLocator::GetModules, cos.iassemblylocator_getmodules
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IAssemblyLocator.GetModules
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAssemblyLocator::GetModules method


## -description


Used to get the names of the modules that are contained in an assembly.


## -parameters




### -param applicationDir [in]

The directory containing the application.


### -param applicationName [in]

The name of the application domain.


### -param assemblyName [in]

The name of the assembly.


### -param pModules [out]

An array listing the names of the modules in the assembly.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/347a209e-be6f-42a9-978f-f40e628fc34b">IAssemblyLocator</a>
 

 

