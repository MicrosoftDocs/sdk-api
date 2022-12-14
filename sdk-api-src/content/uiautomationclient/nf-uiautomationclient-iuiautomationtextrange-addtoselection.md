---
UID: NF:uiautomationclient.IUIAutomationTextRange.AddToSelection
title: IUIAutomationTextRange::AddToSelection (uiautomationclient.h)
description: Adds the text range to the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text. (IUIAutomationTextRange.AddToSelection)
helpviewer_keywords: ["AddToSelection","AddToSelection method [Windows Accessibility]","AddToSelection method [Windows Accessibility]","IUIAutomationTextRange interface","IUIAutomationTextRange interface [Windows Accessibility]","AddToSelection method","IUIAutomationTextRange.AddToSelection","IUIAutomationTextRange::AddToSelection","uiauto.uiauto_IUIAutomationTextRange_AddToSelection","uiauto_IUIAutomationTextRange_AddToSelection","uiautomationclient/IUIAutomationTextRange::AddToSelection","winauto.uiauto_IUIAutomationTextRange_AddToSelection"]
old-location: winauto\uiauto_IUIAutomationTextRange_AddToSelection.htm
tech.root: WinAuto
ms.assetid: 5ae4a131-3283-4e91-8419-f2aa6f488833
ms.date: 12/05/2018
ms.keywords: AddToSelection, AddToSelection method [Windows Accessibility], AddToSelection method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],AddToSelection method, IUIAutomationTextRange.AddToSelection, IUIAutomationTextRange::AddToSelection, uiauto.uiauto_IUIAutomationTextRange_AddToSelection, uiauto_IUIAutomationTextRange_AddToSelection, uiautomationclient/IUIAutomationTextRange::AddToSelection, winauto.uiauto_IUIAutomationTextRange_AddToSelection
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationTextRange::AddToSelection
 - uiautomationclient/IUIAutomationTextRange::AddToSelection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTextRange.AddToSelection
---

# IUIAutomationTextRange::AddToSelection


## -description

Adds the text range to the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The text insertion point moves to the newly selected text. If <b>AddToSelection</b> is called on a text range object that represents a degenerate (empty) text range, the text insertion point moves to the starting endpoint of the text range.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-select">IUIAutomationTextRange::Select</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>
