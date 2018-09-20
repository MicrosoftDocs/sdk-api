---
UID: NE:uiautomationcore.TextEditChangeType
title: TextEditChangeType
author: windows-sdk-content
description: Describes the text editing change being performed by controls when text-edit events are raised or handled.
old-location: winauto\uiauto_TextEditChangeTypeEnum.htm
tech.root: WinAuto
ms.assetid: 212FD71E-BB79-F4A5-061E-F77FF7876998
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: TextEditChangeType, TextEditChangeType enumeration [Windows Accessibility], TextEditChangeType_AutoCorrect, TextEditChangeType_Composition, TextEditChangeType_CompositionFinalized, TextEditChangeType_None, uiautomationcore/TextEditChangeType, uiautomationcore/TextEditChangeType_AutoCorrect, uiautomationcore/TextEditChangeType_Composition, uiautomationcore/TextEditChangeType_CompositionFinalized, uiautomationcore/TextEditChangeType_None, winauto.uiauto_TextEditChangeTypeEnum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

