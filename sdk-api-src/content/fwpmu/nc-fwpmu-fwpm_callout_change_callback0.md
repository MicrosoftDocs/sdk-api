---
UID: NC:fwpmu.FWPM_CALLOUT_CHANGE_CALLBACK0
title: FWPM_CALLOUT_CHANGE_CALLBACK0 (fwpmu.h)

description: Is used to add custom behavior to the callout change notification process.
old-location: fwp\fwpm_callout_change_callback0_func.htm
tech.root: fwp
ms.assetid: 82c678a5-adba-42ea-b85c-4bbdcec78673

ms.date: 12/05/2018
ms.keywords: FWPM_CALLOUT_CHANGE_CALLBACK0, FWPM_CALLOUT_CHANGE_CALLBACK0 callback, FWPM_CALLOUT_CHANGE_CALLBACK0 callback function [Filtering], fwp.fwpm_callout_change_callback0_func, fwpmu/FWPM_CALLOUT_CHANGE_CALLBACK0
ms.topic: callback
f1_keywords: 
 - "fwpmu/FWPM_CALLOUT_CHANGE_CALLBACK0"
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
 - FWPM_CALLOUT_CHANGE_CALLBACK0
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FWPM_CALLOUT_CHANGE_CALLBACK0 callback function


## -description


The <b>FWPM_CALLOUT_CHANGE_CALLBACK0</b> function is used to add custom behavior to the callout change notification process.


## -parameters




### -param *context [in]

Type: <b>void*</b>

Optional context pointer. It contains the value of the <i>context</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0">FwpmCalloutSubscribeChanges0</a> function.


### -param *change [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_callout_change0_">FWPM_CALLOUT_CHANGE0</a>*</b>

The change notification information.


## -returns



This callback function does not return a value.




## -remarks



Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0">FwpmCalloutSubscribeChanges0</a> to register this callback function.

<b>FWPM_CALLOUT_CHANGE_CALLBACK0</b> is a specific implementation of FWPM_CALLOUT_CHANGE_CALLBACK. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_callout_change0_">FWPM_CALLOUT_CHANGE0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0">FwpmCalloutSubscribeChanges0</a>
 

 

