---
UID: NF:uiautomationclient.IUIAutomationTextRange.ScrollIntoView
title: IUIAutomationTextRange::ScrollIntoView (uiautomationclient.h)
description: Causes the text control to scroll until the text range is visible in the viewport.
helpviewer_keywords: ["IUIAutomationTextRange interface [Windows Accessibility]","ScrollIntoView method","IUIAutomationTextRange.ScrollIntoView","IUIAutomationTextRange::ScrollIntoView","ScrollIntoView","ScrollIntoView method [Windows Accessibility]","ScrollIntoView method [Windows Accessibility]","IUIAutomationTextRange interface","uiauto.uiauto_IUIAutomationTextRange_ScrollIntoView","uiauto_IUIAutomationTextRange_ScrollIntoView","uiautomationclient/IUIAutomationTextRange::ScrollIntoView","winauto.uiauto_IUIAutomationTextRange_ScrollIntoView"]
old-location: winauto\uiauto_IUIAutomationTextRange_ScrollIntoView.htm
tech.root: WinAuto
ms.assetid: 0d1ec553-1cc2-4b1c-a393-2507a3756a6c
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextRange interface [Windows Accessibility],ScrollIntoView method, IUIAutomationTextRange.ScrollIntoView, IUIAutomationTextRange::ScrollIntoView, ScrollIntoView, ScrollIntoView method [Windows Accessibility], ScrollIntoView method [Windows Accessibility],IUIAutomationTextRange interface, uiauto.uiauto_IUIAutomationTextRange_ScrollIntoView, uiauto_IUIAutomationTextRange_ScrollIntoView, uiautomationclient/IUIAutomationTextRange::ScrollIntoView, winauto.uiauto_IUIAutomationTextRange_ScrollIntoView
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
 - IUIAutomationTextRange::ScrollIntoView
 - uiautomationclient/IUIAutomationTextRange::ScrollIntoView
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
 - IUIAutomationTextRange.ScrollIntoView
---

# IUIAutomationTextRange::ScrollIntoView


## -description

Causes the text control to scroll until the text range is visible in the viewport.

## -parameters

### -param alignToTop [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the text control should be scrolled so that the text range is flush with the top of the viewport; <b>FALSE</b> if it should be flush with the bottom of the viewport.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The method respects both hidden and visible text. If the text range is hidden, the text control will scroll only if the hidden text has an anchor in the viewport. 

 A Microsoft UI Automation client can check text visibility by calling <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue">IUIAutomationTextRange::GetAttributeValue</a> with the <i>attr</i> parameter set to <a href="/windows/desktop/WinAuto/uiauto-textattribute-ids">UIA_IsHiddenAttributeId</a>.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>