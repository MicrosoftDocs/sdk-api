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

Gets [Interaction Context](../_input_intcontext/index.md) object properties.

## -parameters

### -param interactionContext [in]

Handle to the [Interaction Context](../_input_intcontext/index.md) object.

### -param contextProperty [in]

One of the constants identified by [INTERACTION_CONTEXT_PROPERTY enumeration](ne-interactioncontext-interaction_context_property.md).

### -param value [out]

The value of the property.

Valid values for *contextProperty* are:

|||
|--- |--- |
|**INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS_HIMETRIC**<br>0|Measurement units are HIMETRIC  units (0.01 mm).|
|**INTERACTION_CONTEXT_PROPERTY_MEASUREMENT_UNITS_SCREEN**<br>1|Measurement units are screen pixels. This is the default value.|
|**INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_OFF**<br>0|Visual feedback for user interactions is disabled (the caller is responsible for displaying visual feedback). For more info, see [GetWindowFeedbackSetting function](../winuser/nf-winuser-getwindowfeedbacksetting.md) and [SetWindowFeedbackSetting function](../winuser/nf-winuser-setwindowfeedbacksetting.md)|
|**INTERACTION_CONTEXT_PROPERTY_UI_FEEDBACK_ON**<br>1|Visual feedback for user interactions is enabled. This is the default value. For more info, see [GetWindowFeedbackSetting function](../winuser/nf-winuser-getwindowfeedbacksetting.md) and [SetWindowFeedbackSetting function](../winuser/nf-winuser-setwindowfeedbacksetting.md).|
|**INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS_OFF**<br>0|Pointer filtering is disabled (all pointer input data is processed).|
|**INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS_ON**<br>1|Pointer filtering is enabled (only pointers specified through the [AddPointerInteractionContext function](nf-interactioncontext-addpointerinteractioncontext.md) are processed). This is the default value. |

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -see-also

[SetPropertyInteractionContext function](nf-interactioncontext-setpropertyinteractioncontext.md)
