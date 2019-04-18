---
UID: NC:fwpmu.FWPM_PROVIDER_CHANGE_CALLBACK0
title: FWPM_PROVIDER_CHANGE_CALLBACK0 (fwpmu.h)
author: windows-sdk-content
description: To add custom behavior to the provider change notification process.
old-location: fwp\fwpm_provider_change_callback0_func.htm
tech.root: fwp
ms.assetid: 00f564d3-90b3-449e-a88a-ea5b3d9cff16
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER_CHANGE_CALLBACK0, FWPM_PROVIDER_CHANGE_CALLBACK0 callback, FWPM_PROVIDER_CHANGE_CALLBACK0 callback function [Filtering], fwp.fwpm_provider_change_callback0_func, fwpmu/FWPM_PROVIDER_CHANGE_CALLBACK0
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
 - FWPM_PROVIDER_CHANGE_CALLBACK0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FWPM_PROVIDER_CHANGE_CALLBACK0 callback function


## -description


The <b>FWPM_PROVIDER_CHANGE_CALLBACK0</b> function is used to add custom behavior to the provider change notification process.


## -parameters




### -param *context [in]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter passed to the <a href="https://msdn.microsoft.com/73d04bcb-b888-4e40-90e6-a0d777f926ef">FwpmProviderSubscribeChanges0</a> function.


### -param *change [in]

Type: <b>const <a href="https://msdn.microsoft.com/abd5c40c-5907-4f1e-8fb3-28d43ecebfc8">FWPM_PROVIDER_CHANGE0</a>*</b>

The change notification information.


## -returns



This callback function does not return a value.




## -remarks



Call <a href="https://msdn.microsoft.com/73d04bcb-b888-4e40-90e6-a0d777f926ef">FwpmProviderSubscribeChanges0</a> to register this callback function.

<b>FWPM_PROVIDER_CHANGE_CALLBACK0</b> is a specific implementation of FWPM_PROVIDER_CHANGE_CALLBACK. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/abd5c40c-5907-4f1e-8fb3-28d43ecebfc8">FWPM_PROVIDER_CHANGE0</a>



<a href="https://msdn.microsoft.com/73d04bcb-b888-4e40-90e6-a0d777f926ef">FwpmProviderSubscribeChanges0</a>
 

 

