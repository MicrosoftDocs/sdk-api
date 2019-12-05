---
UID: NE:uiautomationcore.TextEditChangeType
title: TextEditChangeType (uiautomationcore.h)
description: Describes the text editing change being performed by controls when text-edit events are raised or handled.
old-location: winauto\uiauto_TextEditChangeTypeEnum.htm
tech.root: WinAuto
ms.assetid: 212FD71E-BB79-F4A5-061E-F77FF7876998
ms.date: 12/05/2018
ms.keywords: TextEditChangeType, TextEditChangeType enumeration [Windows Accessibility], TextEditChangeType_AutoCorrect, TextEditChangeType_Composition, TextEditChangeType_CompositionFinalized, TextEditChangeType_None, uiautomationcore/TextEditChangeType, uiautomationcore/TextEditChangeType_AutoCorrect, uiautomationcore/TextEditChangeType_Composition, uiautomationcore/TextEditChangeType_CompositionFinalized, uiautomationcore/TextEditChangeType_None, winauto.uiauto_TextEditChangeTypeEnum
ms.topic: enum
f1_keywords:
- uiautomationcore/TextEditChangeType
dev_langs:
- c++
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
- UIAutomationCore.h
api_name:
- TextEditChangeType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itexteditprovider">ITextEditProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-textattribute-ids">Text Attribute Identifiers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent">UiaRaiseTextEditTextChangedEvent function</a>
 

 

