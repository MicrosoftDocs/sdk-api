---
UID: NF:uiautomationclient.IUIAutomationTextPattern.GetSelection
title: IUIAutomationTextPattern::GetSelection (uiautomationclient.h)
description: Retrieves a collection of text ranges that represents the currently selected text in a text-based control. (IUIAutomationTextPattern.GetSelection)
helpviewer_keywords: ["GetSelection","GetSelection method [Windows Accessibility]","GetSelection method [Windows Accessibility]","IUIAutomationTextPattern interface","IUIAutomationTextPattern interface [Windows Accessibility]","GetSelection method","IUIAutomationTextPattern.GetSelection","IUIAutomationTextPattern::GetSelection","uiauto.uiauto_IUIAutomationTextPattern_GetSelection","uiauto_IUIAutomationTextPattern_GetSelection","uiautomationclient/IUIAutomationTextPattern::GetSelection","winauto.uiauto_IUIAutomationTextPattern_GetSelection"]
old-location: winauto\uiauto_IUIAutomationTextPattern_GetSelection.htm
tech.root: WinAuto
ms.assetid: 2aca7414-afb2-402d-80cf-d7ce3e719b20
ms.date: 12/05/2018
ms.keywords: GetSelection, GetSelection method [Windows Accessibility], GetSelection method [Windows Accessibility],IUIAutomationTextPattern interface, IUIAutomationTextPattern interface [Windows Accessibility],GetSelection method, IUIAutomationTextPattern.GetSelection, IUIAutomationTextPattern::GetSelection, uiauto.uiauto_IUIAutomationTextPattern_GetSelection, uiauto_IUIAutomationTextPattern_GetSelection, uiautomationclient/IUIAutomationTextPattern::GetSelection, winauto.uiauto_IUIAutomationTextPattern_GetSelection
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
 - IUIAutomationTextPattern::GetSelection
 - uiautomationclient/IUIAutomationTextPattern::GetSelection
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
 - IUIAutomationTextPattern.GetSelection
---

# IUIAutomationTextPattern::GetSelection


## -description

Retrieves a collection of text ranges that represents the currently selected text in a text-based control.

## -parameters

### -param ranges [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrangearray">IUIAutomationTextRangeArray</a>**</b>

Receives a pointer to the collection of text ranges.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the control supports the selection of multiple, non-contiguous spans of text, the <i>ranges</i> collection receives one text range for each selected span. 

If the control contains only a single span of selected text, the <i>ranges</i> collection receives a single text range. 

If the control contains a text insertion point but no text is selected, the <i>ranges</i> collection receives a degenerate (empty) text range at the position of the text insertion point.

If the control does  not contain a text insertion point or does not support text selection, <i>ranges</i> is set to <b>NULL</b>.

Use the <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextpattern-get_supportedtextselection">IUIAutomationTextPattern::SupportedTextSelection</a> property to test whether a control supports text selection.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>
