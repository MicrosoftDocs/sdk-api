---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# FWPS_FILTER2_ structure


## -description


The <b>FWPS_FILTER2</b> structure defines a run-time filter in the filter engine.<div class="alert"><b>Note</b>  <b>FWPS_FILTER2</b> is the specific version of <b>FWPS_FILTER</b> used in Windows 8 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/library/windows/hardware/ff552389">FWPS_FILTER1</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/library/windows/hardware/ff552387">FWPS_FILTER0</a> is available.</div>
<div> </div>



## -struct-fields




### -field filterId

A run-time identifier that identifies the filter in the filter engine.


### -field weight

An 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552450">FWP_VALUE0</a> structure that contains a value that
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
     <a href="https://msdn.microsoft.com/de8220de-cf71-4718-876e-ef02c15fc948">classifyFn2</a> callout function should take when
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
       <a href="https://msdn.microsoft.com/de8220de-cf71-4718-876e-ef02c15fc948">classifyFn2</a> callout function that it should
       always clear the FWPS_RIGHT_ACTION_WRITE flag when it returns either FWP_ACTION_BLOCK or
       FWP_ACTION_PERMIT for the suggested action. If this flag is not set, a callout's 
       <i>classifyFn2</i> callout function should only
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
       <a href="https://msdn.microsoft.com/de8220de-cf71-4718-876e-ef02c15fc948">classifyFn2</a> callout function that if the
       callout is not registered, the callout should be treated as a permit filter.

</td>
</tr>
</table>
 


### -field numFilterConditions

The number of 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552391">FWPS_FILTER_CONDITION0</a> structures in
     the array pointed to by the 
     <b>filterCondition</b> member. This member can be zero.


### -field filterCondition

A pointer to an array of 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552391">FWPS_FILTER_CONDITION0</a> structures.
     These structures define the run-time filtering conditions for the filter. If the 
     <b>numFilterConditions</b> member is zero, then this pointer will be NULL.


### -field action

An 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff551215">FWPS_ACTION0</a> structure that specifies the
     action that the filter should take if all of the filter's filtering conditions are true.


### -field context

A context value that is associated with the filter. A callout can set this member to point to a
     callout driver-supplied context structure from within the callout driver's 
     <a href="https://msdn.microsoft.com/c70c987b-5b4c-4ddd-8eb8-8c3c40003ab3">notifyFn2</a> callout function when the filter is
     added to the filter engine. This context structure, which is opaque to the filter engine, can be used by
     the callout driver's 
     <a href="https://msdn.microsoft.com/de8220de-cf71-4718-876e-ef02c15fc948">classifyFn2</a> callout function to preserve any
     driver-specific data or state information between calls by the filter engine to the callout driver's 
     <i>classifyFn2</i> callout function.


### -field providerContext

A pointer to the provider context, which is formatted as a <a href="https://msdn.microsoft.com/aa397a4e-07cc-4eee-8d0f-798901a5bb29">FWPM_PROVIDER_CONTEXT2</a> structure. If the filter uses a callout, and the callout has the FWPM_CALLOUT_FLAG_USES_PROVIDER_CONTEXT flag set, this member will contain the provider context from the corresponding <a href="https://msdn.microsoft.com/e1925824-01c2-426a-a8f0-4d5882812a9e">FWPM_FILTER0</a> structure. Otherwise, this parameter is
     NULL. 
     


## -remarks



The filter engine passes a pointer to an <b>FWPS_FILTER2</b> structure to a callout's 
    <a href="https://msdn.microsoft.com/c70c987b-5b4c-4ddd-8eb8-8c3c40003ab3">notifyFn2</a> and 
    <a href="https://msdn.microsoft.com/de8220de-cf71-4718-876e-ef02c15fc948">classifyFn2</a> callout functions.

A filter's action is performed only if all of the filter's filtering conditions are true. If no
    filtering conditions are specified in the filter, then the specified action is always performed.

The 
    <b>providerContext</b> member provides a mechanism for a callout driver to retrieve provider contexts
    without calling the base filtering engine (BFE).

This structure is essentially identical to the previous version, 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff552389">FWPS_FILTER1</a>. The only difference is the updated <a href="https://msdn.microsoft.com/aa397a4e-07cc-4eee-8d0f-798901a5bb29">FWPM_PROVIDER_CONTEXT2</a> structure at the <b>providerContext</b> member.




## -see-also




<a href="https://msdn.microsoft.com/e1925824-01c2-426a-a8f0-4d5882812a9e">FWPM_FILTER0</a>



<a href="https://msdn.microsoft.com/aa397a4e-07cc-4eee-8d0f-798901a5bb29">FWPM_PROVIDER_CONTEXT2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551215">FWPS_ACTION0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552387">FWPS_FILTER0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552389">FWPS_FILTER1</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552391">FWPS_FILTER_CONDITION0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552450">FWP_VALUE0</a>



<a href="https://msdn.microsoft.com/de8220de-cf71-4718-876e-ef02c15fc948">classifyFn2</a>



<a href="https://msdn.microsoft.com/c70c987b-5b4c-4ddd-8eb8-8c3c40003ab3">notifyFn2</a>
 

 

