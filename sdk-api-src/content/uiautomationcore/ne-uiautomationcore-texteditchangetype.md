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

# TextEditChangeType enumeration


## -description


Describes the text editing change being performed by controls when text-edit events are raised or handled.


## -enum-fields




### -field TextEditChangeType_None

Not related to a specific change type.


### -field TextEditChangeType_AutoCorrect

Change is from an auto-correct action performed by a control.


### -field TextEditChangeType_Composition

Change is from an IME active composition within a control.


### -field TextEditChangeType_CompositionFinalized

Change is from an IME composition going from active to finalized state within a control.

<div class="alert"><b>Note</b>  The finalized string may be empty if composition was canceled or deleted.</div>
<div> </div>

### -field TextEditChangeType_AutoComplete




## -see-also




<a href="https://msdn.microsoft.com/6AA3F2A5-B34C-F7CB-13B3-6C62E2B67326">ITextEditProvider</a>



<a href="https://msdn.microsoft.com/67d86817-6a3f-4047-88d9-34f33f52a563">Text Attribute Identifiers</a>



<a href="https://msdn.microsoft.com/19E7C2C1-D0D5-672F-FC6F-8E1B8CC19819">UiaRaiseTextEditTextChangedEvent function</a>
 

 

