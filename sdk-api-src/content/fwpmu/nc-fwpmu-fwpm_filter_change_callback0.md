---
UID: NC:fwpmu.FWPM_FILTER_CHANGE_CALLBACK0
title: FWPM_FILTER_CHANGE_CALLBACK0 (fwpmu.h)
description: Is used to add custom behavior to the filter change notification process.
helpviewer_keywords: ["FWPM_FILTER_CHANGE_CALLBACK0","FWPM_FILTER_CHANGE_CALLBACK0 callback","FWPM_FILTER_CHANGE_CALLBACK0 callback function [Filtering]","fwp.fwpm_filter_change_callback0_func","fwpmu/FWPM_FILTER_CHANGE_CALLBACK0"]
old-location: fwp\fwpm_filter_change_callback0_func.htm
tech.root: fwp
ms.assetid: 6c0c41d7-ff84-4ae3-b9e0-ebc52cc6273d
ms.date: 12/05/2018
ms.keywords: FWPM_FILTER_CHANGE_CALLBACK0, FWPM_FILTER_CHANGE_CALLBACK0 callback, FWPM_FILTER_CHANGE_CALLBACK0 callback function [Filtering], fwp.fwpm_filter_change_callback0_func, fwpmu/FWPM_FILTER_CHANGE_CALLBACK0
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
 - FWPM_FILTER_CHANGE_CALLBACK0
 - fwpmu/FWPM_FILTER_CHANGE_CALLBACK0
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
 - FWPM_FILTER_CHANGE_CALLBACK0
---

# FWPM_FILTER_CHANGE_CALLBACK0 callback function


## -description

The <b>FWPM_FILTER_CHANGE_CALLBACK0</b> function is used to add custom behavior to the filter change notification process.

## -parameters

### -param context [in]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter passed to the <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0">FwpmFilterSubscribeChanges0</a> function.

### -param change [in]

Type: [FWPM_FILTER_CHANGE0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter_change0)*</b>

The change notification information.

## -remarks

Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0">FwpmFilterSubscribeChanges0</a> to register this callback function.

<b>FWPM_FILTER_CHANGE_CALLBACK0</b> is a specific implementation of FWPM_FILTER_CHANGE_CALLBACK. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_FILTER_CHANGE0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter_change0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0">FwpmFilterSubscribeChanges0</a>
