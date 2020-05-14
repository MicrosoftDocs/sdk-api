---
UID: NC:fwpmu.FWPM_PROVIDER_CHANGE_CALLBACK0
title: FWPM_PROVIDER_CHANGE_CALLBACK0 (fwpmu.h)
description: To add custom behavior to the provider change notification process.
helpviewer_keywords: ["FWPM_PROVIDER_CHANGE_CALLBACK0","FWPM_PROVIDER_CHANGE_CALLBACK0 callback","FWPM_PROVIDER_CHANGE_CALLBACK0 callback function [Filtering]","fwp.fwpm_provider_change_callback0_func","fwpmu/FWPM_PROVIDER_CHANGE_CALLBACK0"]
old-location: fwp\fwpm_provider_change_callback0_func.htm
tech.root: fwp
ms.assetid: 00f564d3-90b3-449e-a88a-ea5b3d9cff16
ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER_CHANGE_CALLBACK0, FWPM_PROVIDER_CHANGE_CALLBACK0 callback, FWPM_PROVIDER_CHANGE_CALLBACK0 callback function [Filtering], fwp.fwpm_provider_change_callback0_func, fwpmu/FWPM_PROVIDER_CHANGE_CALLBACK0
f1_keywords:
- fwpmu/FWPM_PROVIDER_CHANGE_CALLBACK0
dev_langs:
- c++
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

Optional context pointer. It contains the value of the <i>context</i> parameter passed to the <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0">FwpmProviderSubscribeChanges0</a> function.


### -param *change [in]

Type: [FWPM_PROVIDER_CHANGE0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_change0)*</b>

The change notification information.


## -remarks



Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0">FwpmProviderSubscribeChanges0</a> to register this callback function.

<b>FWPM_PROVIDER_CHANGE_CALLBACK0</b> is a specific implementation of FWPM_PROVIDER_CHANGE_CALLBACK. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




[FWPM_PROVIDER_CHANGE0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_change0)



<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0">FwpmProviderSubscribeChanges0</a>
 

 

