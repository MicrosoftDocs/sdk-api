---
UID: NS:fwpmtypes.FWPM_FILTER0_
title: FWPM_FILTER0 (fwpmtypes.h)
description: Stores the state associated with a filter.helpviewer_keywords: ["FWPM_FILTER0","FWPM_FILTER0 structure [Filtering]","FWPM_FILTER_FLAG_BOOTTIME","FWPM_FILTER_FLAG_CLEAR_ACTION_RIGHT","FWPM_FILTER_FLAG_DISABLED","FWPM_FILTER_FLAG_HAS_PROVIDER_CONTEXT","FWPM_FILTER_FLAG_INDEXED","FWPM_FILTER_FLAG_NONE","FWPM_FILTER_FLAG_PERMIT_IF_CALLOUT_UNREGISTERED","FWPM_FILTER_FLAG_PERSISTENT","FWP_EMPTY","FWP_UINT64","FWP_UINT8","fwp.fwpm_filter0","fwpmtypes/FWPM_FILTER0"]
old-location: fwp\fwpm_filter0.htm
tech.root: fwp
ms.assetid: e1925824-01c2-426a-a8f0-4d5882812a9e
ms.date: 12/05/2018
ms.keywords: FWPM_FILTER0, FWPM_FILTER0 structure [Filtering], FWPM_FILTER_FLAG_BOOTTIME, FWPM_FILTER_FLAG_CLEAR_ACTION_RIGHT, FWPM_FILTER_FLAG_DISABLED, FWPM_FILTER_FLAG_HAS_PROVIDER_CONTEXT, FWPM_FILTER_FLAG_INDEXED, FWPM_FILTER_FLAG_NONE, FWPM_FILTER_FLAG_PERMIT_IF_CALLOUT_UNREGISTERED, FWPM_FILTER_FLAG_PERSISTENT, FWP_EMPTY, FWP_UINT64, FWP_UINT8, fwp.fwpm_filter0, fwpmtypes/FWPM_FILTER0
f1_keywords:
- fwpmtypes/FWPM_FILTER0
dev_langs:
- c++
req.header: fwpmtypes.h
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
- HeaderDef
api_location:
- Fwpmtypes.h
api_name:
- FWPM_FILTER0
targetos: Windows
req.typenames: FWPM_FILTER0
req.redist: 
ms.custom: 19H1
---

# FWPM_FILTER0 structure


## -description


The <b>FWPM_FILTER0</b> structure stores the state associated with a filter.


## -struct-fields




### -field filterKey

Uniquely identifies the session. 

If the GUID is initialized to zero in the
   call to <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfilteradd0">FwpmFilterAdd0</a>, the Base Filtering Engine (BFE) will generate one.


### -field displayData

A [FWPM_DISPLAY_DATA0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0)a> structure that contains human-readable annotations associated with the filter.  The <b>name</b> member of the <b>FWPM_DISPLAY_DATA0</b> structure is required.


### -field flags

A combination of the following values.

<table>
<tr>
<th>Filter flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_FILTER_FLAG_NONE"></a><a id="fwpm_filter_flag_none"></a><dl>
<dt><b>FWPM_FILTER_FLAG_NONE</b></dt>
</dl>
</td>
<td width="60%">
Default.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_FILTER_FLAG_PERSISTENT"></a><a id="fwpm_filter_flag_persistent"></a><dl>
<dt><b>FWPM_FILTER_FLAG_PERSISTENT</b></dt>
</dl>
</td>
<td width="60%">
Filter is persistent, that is, it survives across BFE stop/start.

<div class="alert"><b>Note</b>  This flag cannot be set together with <b>FWPM_FILTER_FLAG_BOOTTIME</b>.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_FILTER_FLAG_BOOTTIME"></a><a id="fwpm_filter_flag_boottime"></a><dl>
<dt><b>FWPM_FILTER_FLAG_BOOTTIME</b></dt>
</dl>
</td>
<td width="60%">
Filter is enforced at boot-time, even before BFE starts.

<div class="alert"><b>Note</b>  This flag cannot be set together with <b>FWPM_FILTER_FLAG_PERSISTENT</b>.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_FILTER_FLAG_HAS_PROVIDER_CONTEXT"></a><a id="fwpm_filter_flag_has_provider_context"></a><dl>
<dt><b>FWPM_FILTER_FLAG_HAS_PROVIDER_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Filter references a provider context.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_FILTER_FLAG_CLEAR_ACTION_RIGHT"></a><a id="fwpm_filter_flag_clear_action_right"></a><dl>
<dt><b>FWPM_FILTER_FLAG_CLEAR_ACTION_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Clear filter action right.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_FILTER_FLAG_PERMIT_IF_CALLOUT_UNREGISTERED"></a><a id="fwpm_filter_flag_permit_if_callout_unregistered"></a><dl>
<dt><b>FWPM_FILTER_FLAG_PERMIT_IF_CALLOUT_UNREGISTERED</b></dt>
</dl>
</td>
<td width="60%">
If the callout is not registered, the filter is treated as a permit filter.


<div class="alert"><b>Note</b>  This flag can be set only if the <b>action</b> type is <b>FWP_ACTION_CALLOUT_TERMINATING</b> or
<b>FWP_ACTION_CALLOUT_UNKNOWN</b>.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_FILTER_FLAG_DISABLED"></a><a id="fwpm_filter_flag_disabled"></a><dl>
<dt><b>FWPM_FILTER_FLAG_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Filter is disabled. A provider's filters are disabled when the BFE starts if the provider has no associated Windows service name, or if the associated service is not set to auto-start. 

<div class="alert"><b>Note</b>  This flag cannot be set when adding new filters. It can only be returned by BFE when getting or enumerating filters.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_FILTER_FLAG_INDEXED"></a><a id="fwpm_filter_flag_indexed"></a><dl>
<dt><b>FWPM_FILTER_FLAG_INDEXED</b></dt>
</dl>
</td>
<td width="60%">
Filter is indexed to help enable faster lookup during classification.

<div class="alert"><b>Note</b>  Available only in Windows 8 and Windows Server 2012.</div>
<div> </div>
</td>
</tr>
</table>
 


### -field providerKey

Optional GUID of the policy provider that manages this filter. See <a href="https://docs.microsoft.com/windows/desktop/FWP/built-in-provider-identifiers">Built-in Provider Identifiers</a> for a list of predefined policy providers.


### -field providerData

A [FWP_BYTE_BLOB](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_byte_blob)a> structure that contains optional provider-specific data used by providers to store additional context information with the object.


### -field layerKey

GUID of the layer where the filter resides. See <a href="https://docs.microsoft.com/windows/desktop/FWP/management-filtering-layer-identifiers-">Filtering Layer Identifiers</a> for a list of possible values.


### -field subLayerKey

GUID of the sub-layer where the filter resides. See <a href="https://docs.microsoft.com/windows/desktop/FWP/management-filtering-sublayer-identifiers">Filtering Sub-Layer Identifiers</a> for a list of built-in sub-layers.

If this is set to IID_NULL, the filter is added to the default sublayer.


### -field weight


A [FWP_VALUE0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0)a> structure that specifies the weight of the filter. Possible type values for <b>weight</b> are as follows.



<table>
<tr>
<th><b>weight</b> type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWP_UINT64"></a><a id="fwp_uint64"></a><dl>
<dt><b>FWP_UINT64</b></dt>
</dl>
</td>
<td width="60%">
BFE will use the supplied value as the filter's weight.

</td>
</tr>
<tr>
<td width="40%"><a id="FWP_UINT8"></a><a id="fwp_uint8"></a><dl>
<dt><b>FWP_UINT8</b></dt>
<dt>0–15</dt>
</dl>
</td>
<td width="60%">
BFE will use the supplied value as a weight range index and will compute the filter's weight in that range. See <a href="https://docs.microsoft.com/windows/desktop/FWP/filter-weight-assignment">Filter Weight Assignment</a> for more information.

</td>
</tr>
<tr>
<td width="40%"><a id="FWP_EMPTY"></a><a id="fwp_empty"></a><dl>
<dt><b>FWP_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
BFE will automatically assign a weight based on the
   filter conditions.

</td>
</tr>
</table>
 

See <a href="https://docs.microsoft.com/windows/desktop/FWP/filter-weight-identifiers">Filter Weight Identifiers</a> for built-in constants that may be used to compute the filter weight.


### -field numFilterConditions

Number of filter conditions.


### -field filterCondition

Array of  [FWPM_FILTER_CONDITION0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0)a> structures that contain all the filtering conditions. All must be true for the action to be
   performed. In other words, the conditions are evaluated using the AND operator. If no
   conditions are specified, the action is always performed. 

<div class="alert"><b>Note</b>  In Windows 7 and Windows Server 2008 R2, consecutive conditions with the same fieldKey will be evaluated using the OR operator. </div>
<div> </div>

### -field action

A [FWPM_ACTION0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_action0)a> structure that specifies the action to be performed if all the filter conditions are true. 


### -field rawContext

Available when the filter does not have provider context information, that is, <b>flags</b> does not contain <b>FWPM_FILTER_FLAG_HAS_PROVIDER_CONTEXT</b>. See <a href="https://docs.microsoft.com/windows/desktop/FWP/filter-context-identifiers">Filter Context Identifiers</a> for a list of built-in possible values.

The <b>rawContext</b> is placed 'as is' in the <b>context</b> member of the corresponding <b>FWPS_FILTER0</b> structure, which is documented in the WDK.


### -field providerContextKey

Available when the filter has provider context information, that is, <b>flags</b> contains <b>FWPM_FILTER_FLAG_HAS_PROVIDER_CONTEXT</b>. See <a href="https://docs.microsoft.com/windows/desktop/FWP/built-in-provider-context-identifiers">Built-in Provider Context Identifiers</a> for a list of predefined policy  provider contexts.

 The LUID of the provider context specified by the <b>providerContextKey</b> is used to fill in the <b>context</b> member of the corresponding <b>FWPS_FILTER0</b> structure, which is documented in the WDK.


### -field reserved

Reserved for system use.


### -field filterId

LUID identifying the filter. This is also the LUID of the corresponding
   <b>FWPS_FILTER0</b> structure, which is documented in the WDK.


### -field effectiveWeight

An [FWP_VALUE0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0)a> structure that contains the weight assigned to <b>FWPS_FILTER0</b>, which is documented in the WDK. 


## -remarks



The first ten members of this structure contain information supplied when adding objects.

The last members, <b>filterId</b> and <b>effectiveWeight</b>, provides additional information when getting/enumerating objects.

<b>FWPM_FILTER0</b> is a specific implementation of FWPM_FILTER. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




[FWPM_ACTION0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_action0)a>



[FWPM_DISPLAY_DATA0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwpm_display_data0)a>



[FWPM_FILTER_CONDITION0](https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0)a>



[FWP_VALUE0](https://docs.microsoft.com/windows/desktop/api/fwptypes/ns-fwptypes-fwp_value0)a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/filter-weight-assignment">Filter Weight Assignment</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/filter-weight-identifiers">Filter Weight Identifiers</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

