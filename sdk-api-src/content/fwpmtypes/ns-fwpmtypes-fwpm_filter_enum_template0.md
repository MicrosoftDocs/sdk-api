---
UID: NS:fwpmtypes.FWPM_FILTER_ENUM_TEMPLATE0_
title: FWPM_FILTER_ENUM_TEMPLATE0 (fwpmtypes.h)
description: Is used for enumerating filters.
helpviewer_keywords: ["FWPM_FILTER_ENUM_TEMPLATE0","FWPM_FILTER_ENUM_TEMPLATE0 structure [Filtering]","FWP_ACTION_FLAG_CALLOUT","FWP_FILTER_ENUM_FLAG_BEST_TERMINATING_MATCH","FWP_FILTER_ENUM_FLAG_BOOTTIME_ONLY","FWP_FILTER_ENUM_FLAG_INCLUDE_BOOTTIME","FWP_FILTER_ENUM_FLAG_INCLUDE_DISABLED","FWP_FILTER_ENUM_FLAG_SORTED","fwp.fwpm_filter_enum_template0_struct","fwpmtypes/FWPM_FILTER_ENUM_TEMPLATE0"]
old-location: fwp\fwpm_filter_enum_template0_struct.htm
tech.root: fwp
ms.assetid: 5ae77ee2-42b2-4794-afec-80360fe4f4da
ms.date: 05/03/2024
ms.keywords: FWPM_FILTER_ENUM_TEMPLATE0, FWPM_FILTER_ENUM_TEMPLATE0 structure [Filtering], FWP_ACTION_FLAG_CALLOUT, FWP_FILTER_ENUM_FLAG_BEST_TERMINATING_MATCH, FWP_FILTER_ENUM_FLAG_BOOTTIME_ONLY, FWP_FILTER_ENUM_FLAG_INCLUDE_BOOTTIME, FWP_FILTER_ENUM_FLAG_INCLUDE_DISABLED, FWP_FILTER_ENUM_FLAG_SORTED, fwp.fwpm_filter_enum_template0_struct, fwpmtypes/FWPM_FILTER_ENUM_TEMPLATE0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_FILTER_ENUM_TEMPLATE0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_FILTER_ENUM_TEMPLATE0_
 - fwpmtypes/FWPM_FILTER_ENUM_TEMPLATE0_
 - FWPM_FILTER_ENUM_TEMPLATE0
 - fwpmtypes/FWPM_FILTER_ENUM_TEMPLATE0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_FILTER_ENUM_TEMPLATE0
---

## -description

The **FWPM_FILTER_ENUM_TEMPLATE0** structure is used for enumerating filters.

## -struct-fields

### -field providerKey

Uniquely identifies the provider associated with this filter.

### -field layerKey

Layer whose fields are to be enumerated.

### -field enumType

A [FWP_FILTER_ENUM_TYPE](/windows/win32/api/fwptypes/ne-fwptypes-fwp_filter_enum_type) value that determines how the filter conditions are interpreted.

### -field flags

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWP_FILTER_ENUM_FLAG_BEST_TERMINATING_MATCH_"></a><a id="fwp_filter_enum_flag_best_terminating_match_"></a><dl>
<dt><b>FWP_FILTER_ENUM_FLAG_BEST_TERMINATING_MATCH</b></dt>
</dl>
</td>
<td width="60%">
Only return the terminating filter with the highest weight.

</td>
</tr>
<tr>
<td width="40%"><a id="FWP_FILTER_ENUM_FLAG_SORTED"></a><a id="fwp_filter_enum_flag_sorted"></a><dl>
<dt><b>FWP_FILTER_ENUM_FLAG_SORTED</b></dt>
</dl>
</td>
<td width="60%">
Return all matching filters sorted by weight (highest to lowest).

</td>
</tr>
<tr>
<td width="40%"><a id="FWP_FILTER_ENUM_FLAG_BOOTTIME_ONLY"></a><a id="fwp_filter_enum_flag_boottime_only"></a><dl>
<dt><b>FWP_FILTER_ENUM_FLAG_BOOTTIME_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Return only boot-time filters.

</td>
</tr>
<tr>
<td width="40%"><a id="FWP_FILTER_ENUM_FLAG_INCLUDE_BOOTTIME"></a><a id="fwp_filter_enum_flag_include_boottime"></a><dl>
<dt><b>FWP_FILTER_ENUM_FLAG_INCLUDE_BOOTTIME</b></dt>
</dl>
</td>
<td width="60%">
Include boot-time filters; ignored if the <b>FWP_FILTER_ENUM_FLAG_BOOTTIME_ONLY</b> flag is set.
</td>
</tr>

<tr>
<td width="40%"><a id="FWP_FILTER_ENUM_FLAG_INCLUDE_DISABLED"></a><a id="fwp_filter_enum_flag_include_disabled"></a><dl>
<dt><b>FWP_FILTER_ENUM_FLAG_INCLUDE_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Include disabled filters; ignored if the <b>FWP_FILTER_ENUM_FLAG_BOOTTIME_ONLY</b> flag is set.
</td>
</tr>

<tr>
<td width="40%"><a id="FWP_FILTER_ENUM_VALID_FLAGS"></a><a id="fwp_filter_enum_valid_flags"></a><dl>
<dt><b>FWP_FILTER_ENUM_VALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
Combination of <b>FWP_FILTER_ENUM_FLAG_BEST_TERMINATING_MATCH</b> and <b>FWP_FILTER_ENUM_FLAG_SORTED</b>.
</td>
</tr>

</table>

### -field providerContextTemplate

A <a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context_enum_template0">FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</a> structure that is used to limit the number of filters enumerated. If non-**NULL**, only enumerate filters whose provider context matches the template.

### -field numFilterConditions

Number of filter conditions. If zero, then all filters match.

### -field filterCondition

An array of [FWPM_FILTER_CONDITION0](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0) structures that contain distinct filter conditions (duplicated filter conditions will generate an error).

### -field actionMask

Only filters whose action type contains at least one of the bits in **actionMask** will be returned. Using the **FWP_ACTION_** constants directly may not work as intended since they contain multiple bits. Some common examples are in the table below (**^** represents the logical XOR operator).

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
 
<tr>
<td width="40%">
<dl>
<dt>FWP_ACTION_BLOCK ^ FWP_ACTION_FLAG_TERMINATING</dt>
</dl>
</td>
<td width="60%">
 Enumerate filters that have an **FWP_ACTION_BLOCK** action.
 </td>
</tr>
 
<tr>
<td width="40%">
<dl>
<dt>FWP_ACTION_PERMIT ^ FWP_ACTION_FLAG_TERMINATING</dt>
</dl>
</td>
<td width="60%">
 Enumerate filters that have an **FWP_ACTION_PERMIT** action.
 </td>
</tr>
 
<tr>
<td width="40%"><a id="FWP_ACTION_FLAG_CALLOUT"></a><a id="fwp_action_flag_callout"></a><dl>
<dt>**FWP_ACTION_FLAG_CALLOUT**</dt>
</dl>
</td>
<td width="60%">
Enumerate filters that reference callout drivers.
<div class="alert">**Note**  **calloutKey** must not be **NULL**.</div>
<div> </div>
</td>
</tr>
 
<tr>
<td width="40%">
<dl>
<dt>0xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
Ignore the filter's action type when enumerating.
</td>
</tr>

</table>

### -field calloutKey

Uniquely identifies the callout.

## -remarks

**FWPM_FILTER_ENUM_TEMPLATE0** is a specific implementation of FWPM_FILTER_ENUM_TEMPLATE. See <a href="/windows/win32/fwp/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_FILTER_CONDITION0](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0)



<a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context_enum_template0">FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</a>



[FWP_FILTER_ENUM_TYPE](/windows/win32/api/fwptypes/ne-fwptypes-fwp_filter_enum_type)



<a href="/windows/win32/fwp/fwp-structs">Windows Filtering Platform  API Structures</a>
