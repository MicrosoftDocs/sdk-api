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

# IUIAutomationTextPattern::GetSelection


## -description


Retrieves a collection of text ranges that represents the currently selected text in a text-based control.  


## -parameters




### -param ranges [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9f059173-7539-4164-b7af-182fa851d11a">IUIAutomationTextRangeArray</a>**</b>

Receives a pointer to the collection of text ranges.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the control supports the selection of multiple, non-contiguous spans of text, the <i>ranges</i> collection receives one text range for each selected span. 

If the control contains only a single span of selected text, the <i>ranges</i> collection receives a single text range. 

If the control contains a text insertion point but no text is selected, the <i>ranges</i> collection receives a degenerate (empty) text range at the position of the text insertion point.

If the control does  not contain a text insertion point or does not support text selection, <i>ranges</i> is set to <b>NULL</b>.

Use the <a href="https://msdn.microsoft.com/794c08d4-9305-4fdd-8ca0-188e1e9b6547">IUIAutomationTextPattern::SupportedTextSelection</a> property to test whether a control supports text selection.




## -see-also




<a href="https://msdn.microsoft.com/ddcf7ecd-7ed2-4b57-82a7-c7e1608dbfa1">IUIAutomationTextPattern</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

