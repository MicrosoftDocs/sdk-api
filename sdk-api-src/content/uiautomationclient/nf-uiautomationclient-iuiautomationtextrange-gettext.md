---
UID: NF:uiautomationclient.IUIAutomationTextRange.GetText
title: IUIAutomationTextRange::GetText (uiautomationclient.h)
description: Returns the plain text of the text range.
helpviewer_keywords: ["GetText","GetText method [Windows Accessibility]","GetText method [Windows Accessibility]","IUIAutomationTextRange interface","IUIAutomationTextRange interface [Windows Accessibility]","GetText method","IUIAutomationTextRange.GetText","IUIAutomationTextRange::GetText","uiauto.uiauto_IUIAutomationTextRange_GetText","uiauto_IUIAutomationTextRange_GetText","uiautomationclient/IUIAutomationTextRange::GetText","winauto.uiauto_IUIAutomationTextRange_GetText"]
old-location: winauto\uiauto_IUIAutomationTextRange_GetText.htm
tech.root: WinAuto
ms.assetid: 704e222d-1e1e-4953-bfa1-bbaa1c5ba833
ms.date: 12/05/2018
ms.keywords: GetText, GetText method [Windows Accessibility], GetText method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],GetText method, IUIAutomationTextRange.GetText, IUIAutomationTextRange::GetText, uiauto.uiauto_IUIAutomationTextRange_GetText, uiauto_IUIAutomationTextRange_GetText, uiautomationclient/IUIAutomationTextRange::GetText, winauto.uiauto_IUIAutomationTextRange_GetText
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
 - IUIAutomationTextRange::GetText
 - uiautomationclient/IUIAutomationTextRange::GetText
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
 - IUIAutomationTextRange.GetText
---

# IUIAutomationTextRange::GetText


## -description

Returns the plain text of the text range.

## -parameters

### -param maxLength [in]

Type: <b>int</b>

The maximum length of the string to return, or -1 if no limit is required.

### -param text [out, retval]

Type: <b>BSTR*</b>

Receives a pointer to the string, possibly truncated at the specified <i>maxLength</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>