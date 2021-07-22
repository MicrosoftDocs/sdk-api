---
UID: NF:uiautomationclient.IUIAutomationTextRange.FindText
title: IUIAutomationTextRange::FindText (uiautomationclient.h)
description: Retrieves a text range subset that contains the specified text.
helpviewer_keywords: ["FindText","FindText method [Windows Accessibility]","FindText method [Windows Accessibility]","IUIAutomationTextRange interface","IUIAutomationTextRange interface [Windows Accessibility]","FindText method","IUIAutomationTextRange.FindText","IUIAutomationTextRange::FindText","uiauto.uiauto_IUIAutomationTextRange_FindText","uiauto_IUIAutomationTextRange_FindText","uiautomationclient/IUIAutomationTextRange::FindText","winauto.uiauto_IUIAutomationTextRange_FindText"]
old-location: winauto\uiauto_IUIAutomationTextRange_FindText.htm
tech.root: WinAuto
ms.assetid: 1d6e9216-747b-45b5-90ac-ec19d36e5a0a
ms.date: 12/05/2018
ms.keywords: FindText, FindText method [Windows Accessibility], FindText method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],FindText method, IUIAutomationTextRange.FindText, IUIAutomationTextRange::FindText, uiauto.uiauto_IUIAutomationTextRange_FindText, uiauto_IUIAutomationTextRange_FindText, uiautomationclient/IUIAutomationTextRange::FindText, winauto.uiauto_IUIAutomationTextRange_FindText
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
 - IUIAutomationTextRange::FindText
 - uiautomationclient/IUIAutomationTextRange::FindText
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
 - IUIAutomationTextRange.FindText
---

# IUIAutomationTextRange::FindText


## -description

Retrieves a text range subset that contains the specified text.

## -parameters

### -param text [in]

Type: <b>BSTR</b>

The text to find.

### -param backward [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the last occurring text range should be returned instead of the first; otherwise <b>FALSE</b>.

### -param ignoreCase [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if case should be ignored; otherwise <b>FALSE</b>.

### -param found [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>**</b>

Receives a pointer to the text range, or <b>NULL</b> if no match is found.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

There is no differentiation between hidden and visible text.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>