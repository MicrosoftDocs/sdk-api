---
UID: NS:fwpstypes.FWPS_FILTER1_
title: FWPS_FILTER1 (fwpstypes.h)
author: windows-sdk-content
description: The FWPS_FILTER1 structure defines a run-time filter in the filter engine.Note  FWPS_FILTER1 is the specific version of FWPS_FILTER used in Windows 7 and later.
old-location: netvista\fwps_filter1.htm
tech.root: NetVista
ms.assetid: 3a5f6f0a-0162-4e64-b3c1-60021ef2dd95
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPS_FILTER1, FWPS_FILTER1 structure [Network Drivers Starting with Windows Vista], FWPS_FILTER_FLAG_CLEAR_ACTION_RIGHT, FWPS_FILTER_FLAG_PERMIT_IF_CALLOUT_UNREGISTERED, fwpstypes/FWPS_FILTER1, netvista.fwps_filter1, wfp_ref_3_struct_3_fwps_F-O_4091c3ca-8d86-4a94-a138-01a6ce09cca8.xml
ms.topic: struct
req.header: fwpstypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 7.
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwpstypes.h
api_name:
 - FWPS_FILTER1
product: Windows
targetos: Windows
req.typenames: FWPS_FILTER1
req.redist: 
---

# FWPS_FILTER1 structure


## -description


The <b>FWPS_FILTER1</b> structure defines a run-time filter in the filter engine.
<div class="alert"><b>Note</b>  <b>FWPS_FILTER1</b> is the specific version of <b>FWPS_FILTER</b> used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/2be2c82b-5b7c-4027-b2a1-f43d2b27b860">FWPS_FILTER2</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/cf5e3372-466e-44f0-8312-78318c5efb13">FWPS_FILTER0</a> is available.</div><div> </div>

## -struct-fields




### -field filterId

A run-time identifier that identifies the filter in the filter engine.


### -field weight

An 
     <a href="https://msdn.microsoft.com/0d8557cd-bd11-4786-ba6e-fbbeb2e2b761">FWP_VALUE0</a> structure that contains a value that
     specifies the filter's importance in relation to other filters in the filter engine. Filters with a
     higher 
     <b>weight</b> value are invoked first. The data type specified in the 
     <b>FWP_VALUE0</b> structure is either <b>FWP_UINT64</b> or
     FWP_EMPTY. If the data type specified in the 
     <b>FWP_VALUE0</b> structure is FWP_EMPTY, the filter
     engine automatically assigns a weight to the filter based on how specific the filter tests the data
     compared to the other filters in the filter engine.


### -field subLayerWeight

A value that specifies the importance of the filter's sublayer in relation to the other sublayers
     in the filter engine. Filters that are located in a sublayer with a higher 
     <b>subLayerWeight</b> value are invoked first.


### -field flags

Flags that specify actions that a callout's 
     <a href="https://msdn.microsoft.com/128fd929-6e83-46a0-9475-e459ede58f30">classifyFn1</a> callout function should take when
     processing network data. Possible flags are:
     

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPS_FILTER_FLAG_CLEAR_ACTION_RIGHT"></a><a id="fwps_filter_flag_clear_action_right"></a><dl>
<dt><b>FWPS_FILTER_FLAG_CLEAR_ACTION_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
This flag indicates to a callout's 
       <a href="https://msdn.microsoft.com/128fd929-6e83-46a0-9475-e459ede58f30">classifyFn1</a> callout function that it should
       always clear the FWPS_RIGHT_ACTION_WRITE flag when it returns either FWP_ACTION_BLOCK or
       FWP_ACTION_PERMIT for the suggested action. If this flag is not set, a callout's 
       <i>classifyFn1</i> callout function should only
       clear the FWPS_RIGHT_ACTION_WRITE flag when it returns FWP_ACTION_BLOCK for the suggested
       action.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPS_FILTER_FLAG_PERMIT_IF_CALLOUT_UNREGISTERED"></a><a id="fwps_filter_flag_permit_if_callout_unregistered"></a><dl>
<dt><b>FWPS_FILTER_FLAG_PERMIT_IF_CALLOUT_UNREGISTERED</b></dt>
</dl>
</td>
<td width="60%">
This flag indicates to a callout's 
       <a href="https://msdn.microsoft.com/128fd929-6e83-46a0-9475-e459ede58f30">classifyFn1</a> callout function that if the
       callout is not registered, the callout should be treated as a permit filter.

</td>
</tr>
</table>
 


### -field numFilterConditions

The number of 
     <a href="https://msdn.microsoft.com/d4a20939-4866-4402-9b29-d94c2170807c">FWPS_FILTER_CONDITION0</a> structures in
     the array pointed to by the 
     <b>filterCondition</b> member. This member can be zero.


### -field filterCondition

A pointer to an array of 
     <a href="https://msdn.microsoft.com/d4a20939-4866-4402-9b29-d94c2170807c">FWPS_FILTER_CONDITION0</a> structures.
     These structures define the run-time filtering conditions for the filter. If the 
     <b>numFilterConditions</b> member is zero, then this pointer will be <b>NULL</b>.


### -field action

An 
     <a href="https://msdn.microsoft.com/1b192efc-e685-48bf-bf61-1419ce03a77a">FWPS_ACTION0</a> structure that specifies the
     action that the filter should take if all of the filter's filtering conditions are true.


### -field context

A context value that is associated with the filter. A callout can set this member to point to a
     callout driver-supplied context structure from within the callout driver's 
     <a href="https://msdn.microsoft.com/3f377049-cc5f-427d-9b09-5e49e4b305c5">notifyFn1</a> callout function when the filter is
     added to the filter engine. This context structure, which is opaque to the filter engine, can be used by
     the callout driver's 
     <a href="https://msdn.microsoft.com/128fd929-6e83-46a0-9475-e459ede58f30">classifyFn1</a> callout function to preserve any
     driver-specific data or state information between calls by the filter engine to the callout driver's 
     <i>classifyFn1</i> callout function.


### -field providerContext

A pointer to the provider context, which is formatted as a <a href="https://msdn.microsoft.com/34727579-9baf-4d50-b973-e864ddf651b0">FWPM_PROVIDER_CONTEXT1</a> structure. If the filter uses a callout, and the callout has the FWPM_CALLOUT_FLAG_USES_PROVIDER_CONTEXT flag set, this member will contain the provider context from the corresponding <a href="https://msdn.microsoft.com/e1925824-01c2-426a-a8f0-4d5882812a9e">FWPM_FILTER0</a> structure. Otherwise, this parameter is
     <b>NULL</b>. 
     


## -remarks



The filter engine passes a pointer to an <b>FWPS_FILTER1</b> structure to a callout's 
    <a href="https://msdn.microsoft.com/3f377049-cc5f-427d-9b09-5e49e4b305c5">notifyFn1</a> and 
    <a href="https://msdn.microsoft.com/128fd929-6e83-46a0-9475-e459ede58f30">classifyFn1</a> callout functions.

A filter's action is performed only if all of the filter's filtering conditions are true. If no
    filtering conditions are specified in the filter, then the specified action is always performed.

The 
    <b>ProviderContext</b> member provides a mechanism for a callout driver to retrieve provider contexts
    without calling the base filtering engine (BFE).




## -see-also




<a href="https://msdn.microsoft.com/a6f19d6d-4fce-4774-86c1-10d1bf77315f">FWPM_CALLOUT0</a>



<a href="https://msdn.microsoft.com/e1925824-01c2-426a-a8f0-4d5882812a9e">FWPM_FILTER0</a>



<a href="https://msdn.microsoft.com/34727579-9baf-4d50-b973-e864ddf651b0">FWPM_PROVIDER_CONTEXT1</a>



<a href="https://msdn.microsoft.com/1b192efc-e685-48bf-bf61-1419ce03a77a">FWPS_ACTION0</a>



<a href="https://msdn.microsoft.com/cf5e3372-466e-44f0-8312-78318c5efb13">FWPS_FILTER0</a>



<a href="https://msdn.microsoft.com/2be2c82b-5b7c-4027-b2a1-f43d2b27b860">FWPS_FILTER2</a>



<a href="https://msdn.microsoft.com/d4a20939-4866-4402-9b29-d94c2170807c">FWPS_FILTER_CONDITION0</a>



<a href="https://msdn.microsoft.com/0d8557cd-bd11-4786-ba6e-fbbeb2e2b761">FWP_VALUE0</a>



<a href="https://msdn.microsoft.com/128fd929-6e83-46a0-9475-e459ede58f30">classifyFn1</a>



<a href="https://msdn.microsoft.com/3f377049-cc5f-427d-9b09-5e49e4b305c5">notifyFn1</a>
 

 

