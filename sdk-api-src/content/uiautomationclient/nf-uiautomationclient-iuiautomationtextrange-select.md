---
UID: NF:uiautomationclient.IUIAutomationTextRange.Select
title: IUIAutomationTextRange::Select (uiautomationclient.h)
description: Selects the span of text that corresponds to this text range, and removes any previous selection. (IUIAutomationTextRange.Select)
helpviewer_keywords: ["IUIAutomationTextRange interface [Windows Accessibility]","Select method","IUIAutomationTextRange.Select","IUIAutomationTextRange::Select","Select","Select method [Windows Accessibility]","Select method [Windows Accessibility]","IUIAutomationTextRange interface","uiauto.uiauto_IUIAutomationTextRange_Select","uiauto_IUIAutomationTextRange_Select","uiautomationclient/IUIAutomationTextRange::Select","winauto.uiauto_IUIAutomationTextRange_Select"]
old-location: winauto\uiauto_IUIAutomationTextRange_Select.htm
tech.root: WinAuto
ms.assetid: 19e8dfe2-bf58-4ea1-8274-4e914f86ba07
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextRange interface [Windows Accessibility],Select method, IUIAutomationTextRange.Select, IUIAutomationTextRange::Select, Select, Select method [Windows Accessibility], Select method [Windows Accessibility],IUIAutomationTextRange interface, uiauto.uiauto_IUIAutomationTextRange_Select, uiauto_IUIAutomationTextRange_Select, uiautomationclient/IUIAutomationTextRange::Select, winauto.uiauto_IUIAutomationTextRange_Select
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
 - IUIAutomationTextRange::Select
 - uiautomationclient/IUIAutomationTextRange::Select
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
 - IUIAutomationTextRange.Select
---

# IUIAutomationTextRange::Select


## -description

Selects the span of text that corresponds to this text range, and removes any previous  selection.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the <b>Select</b> method is called on a text range object that represents a degenerate (empty) text range, the text insertion point moves to the starting endpoint of the text range.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-addtoselection">IUIAutomationTextRange::AddToSelection</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>
