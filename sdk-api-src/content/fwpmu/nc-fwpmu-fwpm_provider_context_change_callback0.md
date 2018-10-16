---
UID: NC:fwpmu.FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0
title: FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0
author: windows-sdk-content
description: Is used to add custom behavior to the provider context change notification process.
old-location: fwp\fwpm_provider_context_change_callback0_func.htm
tech.root: fwp
ms.assetid: 21628bab-ee4d-40e8-8042-97d5462c1013
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0, FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0 callback, FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0 callback function [Filtering], fwp.fwpm_provider_context_change_callback0_func, fwpmu/FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - UserDefined
api_location:
 - Fwpmu.h
api_name:
 - FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0 callback function


## -description


The <b>FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0</b> function is used to add custom behavior to the provider context change notification process.


## -parameters




### -param *context [in]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter passed to the <a href="https://msdn.microsoft.com/cd8c9ec5-c93c-45e5-8a91-88bd89e465d7">FwpmProviderContextSubscribeChanges0</a> function.


### -param *change [in]

Type: <b>const <a href="https://msdn.microsoft.com/78786d91-1e2f-4846-9636-8d5d6acf5a7d">FWPM_PROVIDER_CONTEXT_CHANGE0</a>*</b>

The change notification information.


## -returns



This callback function does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/cd8c9ec5-c93c-45e5-8a91-88bd89e465d7">FwpmProviderContextSubscribeChanges0</a> to register this callback function.

<b>FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0</b> is a specific implementation of FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/78786d91-1e2f-4846-9636-8d5d6acf5a7d">FWPM_PROVIDER_CONTEXT_CHANGE0</a>



<a href="https://msdn.microsoft.com/cd8c9ec5-c93c-45e5-8a91-88bd89e465d7">FwpmProviderContextSubscribeChanges0</a>
 

 

