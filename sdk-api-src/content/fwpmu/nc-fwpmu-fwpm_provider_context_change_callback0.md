---
UID: NC:fwpmu.FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0
title: FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0 (fwpmu.h)
description: Is used to add custom behavior to the provider context change notification process.
helpviewer_keywords: ["FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0","FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0 callback","FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0 callback function [Filtering]","fwp.fwpm_provider_context_change_callback0_func","fwpmu/FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0"]
old-location: fwp\fwpm_provider_context_change_callback0_func.htm
tech.root: fwp
ms.assetid: 21628bab-ee4d-40e8-8042-97d5462c1013
ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0, FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0 callback, FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0 callback function [Filtering], fwp.fwpm_provider_context_change_callback0_func, fwpmu/FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0
 - fwpmu/FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Fwpmu.h
api_name:
 - FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0
---

# FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0 callback function


## -description

The <b>FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0</b> function is used to add custom behavior to the provider context change notification process.

## -parameters

### -param context [in]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter passed to the <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextsubscribechanges0">FwpmProviderContextSubscribeChanges0</a> function.

### -param change [in]

Type: [FWPM_PROVIDER_CONTEXT_CHANGE0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context_change0)*</b>

The change notification information.

## -remarks

Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextsubscribechanges0">FwpmProviderContextSubscribeChanges0</a> to register this callback function.

<b>FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK0</b> is a specific implementation of FWPM_PROVIDER_CONTEXT_CHANGE_CALLBACK. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_PROVIDER_CONTEXT_CHANGE0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context_change0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextsubscribechanges0">FwpmProviderContextSubscribeChanges0</a>
