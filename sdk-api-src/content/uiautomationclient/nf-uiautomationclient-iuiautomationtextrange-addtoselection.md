---
UID: NF:uiautomationclient.IUIAutomationTextRange.AddToSelection
title: IUIAutomationTextRange::AddToSelection method
author: windows-driver-content
description: Adds the text range to the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.
old-location: winauto\uiauto_IUIAutomationTextRange_AddToSelection.htm
old-project: WinAuto
ms.assetid: 5ae4a131-3283-4e91-8419-f2aa6f488833
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: AddToSelection method [Windows Accessibility], AddToSelection method [Windows Accessibility], IUIAutomationTextRange interface, AddToSelection,IUIAutomationTextRange.AddToSelection, IUIAutomationTextRange, IUIAutomationTextRange interface [Windows Accessibility], AddToSelection method, IUIAutomationTextRange::AddToSelection, uiauto.uiauto_IUIAutomationTextRange_AddToSelection, uiauto_IUIAutomationTextRange_AddToSelection, uiautomationclient/IUIAutomationTextRange::AddToSelection, winauto.uiauto_IUIAutomationTextRange_AddToSelection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationClient.h
api_name:
-	IUIAutomationTextRange.AddToSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTextRange::AddToSelection method


## -description


Adds the text range to the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The text insertion point moves to the newly selected text. If <b>AddToSelection</b> is called on a text range object that represents a degenerate (empty) text range, the text insertion point moves to the starting endpoint of the text range.




## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/19e8dfe2-bf58-4ea1-8274-4e914f86ba07">IUIAutomationTextRange::Select</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

