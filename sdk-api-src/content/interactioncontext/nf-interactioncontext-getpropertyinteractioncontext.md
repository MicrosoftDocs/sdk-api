---
UID: NF:interactioncontext.GetPropertyInteractionContext
title: GetPropertyInteractionContext function (interactioncontext.h)
description: Gets Interaction Context object properties.
helpviewer_keywords: ["GetPropertyInteractionContext","GetPropertyInteractionContext function","INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS_OFF","INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS_ON","INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS_HIMETRIC","INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS_SCREEN","INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_OFF","INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_ON","input_intcontext.getpropertyinteractioncontext","interactioncontext.getpropertyinteractioncontext","interactioncontext/GetPropertyInteractionContext"]
old-location: input_intcontext\getpropertyinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: c54a3632-aa7a-416b-b9ed-5ad552403985
ms.date: 12/05/2018
ms.keywords: GetPropertyInteractionContext, GetPropertyInteractionContext function, INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS_OFF, INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS_ON, INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS_HIMETRIC, INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS_SCREEN, INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_OFF, INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_ON, input_intcontext.getpropertyinteractioncontext, interactioncontext.getpropertyinteractioncontext, interactioncontext/GetPropertyInteractionContext
req.header: interactioncontext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetPropertyInteractionContext
 - interactioncontext/GetPropertyInteractionContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ninput.dll
 - API-MS-Win-Input-IE-InteractionContext-l1-1-0.dll
 - IE_Shims.dll
api_name:
 - GetPropertyInteractionContext
---

# GetPropertyInteractionContext function


## -description

Gets <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object properties.

## -parameters

### -param interactionContext [in]

Handle to the <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.

### -param contextProperty [in]

One of the constants identified by <a href="/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-interaction_context_property">INTERACTION_CONTEXT_PROPERTY</a>.

### -param value [out]

The value of the property.

Valid values for <i>contextProperty</i> are:

<table>
<tr>
<th>
<a href="/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-interaction_context_property">INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS</a>
</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS_HIMETRIC"></a><a id="interaction_context_property_measurement_units_himetric"></a><dl>
<dt><b>INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS_HIMETRIC</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Measurement units are HIMETRIC  units (0.01 mm).

</td>
</tr>
<tr>
<td width="40%"><a id="INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS_SCREEN"></a><a id="interaction_context_property_measurement_units_screen"></a><dl>
<dt><b>INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS_SCREEN</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Measurement units are screen pixels. This is the default value.

</td>
</tr>
</table>
 

<table>
<tr>
<th>
<a href="/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-interaction_context_property">INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK</a>
</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_OFF"></a><a id="interaction_context_property_ui_feedback_off"></a><dl>
<dt><b>INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_OFF</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Visual feedback for user interactions is disabled (the caller is responsible for displaying visual feedback). For more info, see <a href="/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal">Input Feedback Configuration</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_ON"></a><a id="interaction_context_property_ui_feedback_on"></a><dl>
<dt><b>INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_ON</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Visual feedback for user interactions is enabled. This is the default value. For more info, see <a href="/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal">Input Feedback Configuration</a>.

</td>
</tr>
</table>
 

<table>
<tr>
<th>INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS_OFF"></a><a id="interaction_context_property_filter_pointers_off"></a><dl>
<dt><b>INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS_OFF</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Pointer filtering is disabled (all pointer input data is processed).

</td>
</tr>
<tr>
<td width="40%"><a id="INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS_ON"></a><a id="interaction_context_property_filter_pointers_on"></a><dl>
<dt><b>INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS_ON</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Pointer filtering is enabled (only pointers specified through <a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext">AddPointerInteractionContext</a> are processed). This is the default value. 

</td>
</tr>
</table>

## -returns

If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.

## -see-also

<a href="/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext">SetPropertyInteractionContext</a>