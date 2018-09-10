---
UID: NF:interactioncontext.GetPropertyInteractionContext
title: GetPropertyInteractionContext function
author: windows-sdk-content
description: Gets Interaction Context object properties.
old-location: input_intcontext\getpropertyinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: c54a3632-aa7a-416b-b9ed-5ad552403985
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetPropertyInteractionContext, GetPropertyInteractionContext function, INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS_OFF, INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS_ON, INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS_HIMETRIC, INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS_SCREEN, INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_OFF, INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_ON, input_intcontext.getpropertyinteractioncontext, interactioncontext.getpropertyinteractioncontext, interactioncontext/GetPropertyInteractionContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPropertyInteractionContext function


## -description


Gets <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object properties.


## -parameters




### -param interactionContext [in]

Handle to the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object. 


### -param contextProperty [in]

One of the constants identified by <a href="https://msdn.microsoft.com/b5b96b33-212e-4e1a-89f6-ee9f94de84aa">INTERACTION_CONTEXT_PROPERTY</a>.


### -param value [out]

The value of the property.

Valid values for <i>contextProperty</i> are:

<table>
<tr>
<th>
<a href="https://msdn.microsoft.com/b5b96b33-212e-4e1a-89f6-ee9f94de84aa">INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS</a>
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
<a href="https://msdn.microsoft.com/b5b96b33-212e-4e1a-89f6-ee9f94de84aa">INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK</a>
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
Visual feedback for user interactions is disabled (the caller is responsible for displaying visual feedback). For more info, see <a href="https://msdn.microsoft.com/9158A6C6-5BB5-4C5C-8411-AE07966B478B">Input Feedback Configuration</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_ON"></a><a id="interaction_context_property_ui_feedback_on"></a><dl>
<dt><b>INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_ON</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Visual feedback for user interactions is enabled. This is the default value. For more info, see <a href="https://msdn.microsoft.com/9158A6C6-5BB5-4C5C-8411-AE07966B478B">Input Feedback Configuration</a>.

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
Pointer filtering is enabled (only pointers specified through <a href="https://msdn.microsoft.com/a720284f-af50-4e55-ae48-c78a1e826dc4">AddPointerInteractionContext</a> are processed). This is the default value. 

</td>
</tr>
</table>
 


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>



<a href="https://msdn.microsoft.com/da24831e-9f9f-4a9f-92bf-60e1c5338554">SetPropertyInteractionContext</a>
 

 

