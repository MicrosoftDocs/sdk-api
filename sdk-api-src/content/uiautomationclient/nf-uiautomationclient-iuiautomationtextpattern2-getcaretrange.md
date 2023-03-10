---
UID: NF:uiautomationclient.IUIAutomationTextPattern2.GetCaretRange
title: IUIAutomationTextPattern2::GetCaretRange (uiautomationclient.h)
description: Retrieves a zero-length text range at the location of the caret that belongs to the text-based control.
helpviewer_keywords: ["GetCaretRange","GetCaretRange method [Windows Accessibility]","GetCaretRange method [Windows Accessibility]","IUIAutomationTextPattern2 interface","IUIAutomationTextPattern2 interface [Windows Accessibility]","GetCaretRange method","IUIAutomationTextPattern2.GetCaretRange","IUIAutomationTextPattern2::GetCaretRange","uiautomationclient/IUIAutomationTextPattern2::GetCaretRange","winauto.uiauto_IUIAutomationTextPattern2_GetCaretRange"]
old-location: winauto\uiauto_IUIAutomationTextPattern2_GetCaretRange.htm
tech.root: WinAuto
ms.assetid: EDB53C04-142E-4DCC-8DD7-F7DD4BC6A67F
ms.date: 12/05/2018
ms.keywords: GetCaretRange, GetCaretRange method [Windows Accessibility], GetCaretRange method [Windows Accessibility],IUIAutomationTextPattern2 interface, IUIAutomationTextPattern2 interface [Windows Accessibility],GetCaretRange method, IUIAutomationTextPattern2.GetCaretRange, IUIAutomationTextPattern2::GetCaretRange, uiautomationclient/IUIAutomationTextPattern2::GetCaretRange, winauto.uiauto_IUIAutomationTextPattern2_GetCaretRange
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IUIAutomationTextPattern2::GetCaretRange
 - uiautomationclient/IUIAutomationTextPattern2::GetCaretRange
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
 - IUIAutomationTextPattern2.GetCaretRange
---

# IUIAutomationTextPattern2::GetCaretRange


## -description

Retrieves a zero-length text range at the location of the caret that belongs to the text-based control.

## -parameters

### -param isActive [out, retval]

Type: <b>BOOL*</b>

<b>TRUE</b> if the text-based control that contains the caret has keyboard focus, otherwise <b>FALSE</b>.

### -param range [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>**</b>

Receives a text range that represents the current location of the caret that belongs to the text-based control.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the <i>isActive</i> parameter is <b>FALSE</b>, the caret that belongs to the text-based control might not be at the same location as the system caret.

This method retrieves a text range that a client can use to find the bounding rectangle of the caret belonging to the text-based control, or to find the text near the caret.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern2">IUIAutomationTextPattern2</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>



<a href="/windows/desktop/WinAuto/uiauto-workingwithtextbasedcontrols">Working with Text-based Controls</a>