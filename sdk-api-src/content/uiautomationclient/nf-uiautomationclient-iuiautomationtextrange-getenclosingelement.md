---
UID: NF:uiautomationclient.IUIAutomationTextRange.GetEnclosingElement
title: IUIAutomationTextRange::GetEnclosingElement (uiautomationclient.h)
description: Returns the innermost UI Automation element that encloses the text range.
helpviewer_keywords: ["GetEnclosingElement","GetEnclosingElement method [Windows Accessibility]","GetEnclosingElement method [Windows Accessibility]","IUIAutomationTextRange interface","IUIAutomationTextRange interface [Windows Accessibility]","GetEnclosingElement method","IUIAutomationTextRange.GetEnclosingElement","IUIAutomationTextRange::GetEnclosingElement","uiauto.uiauto_IUIAutomationTextRange_GetEnclosingElement","uiauto_IUIAutomationTextRange_GetEnclosingElement","uiautomationclient/IUIAutomationTextRange::GetEnclosingElement","winauto.uiauto_IUIAutomationTextRange_GetEnclosingElement"]
old-location: winauto\uiauto_IUIAutomationTextRange_GetEnclosingElement.htm
tech.root: WinAuto
ms.assetid: 0120b4af-6f08-4bbd-b649-0f8e84cda3b9
ms.date: 12/05/2018
ms.keywords: GetEnclosingElement, GetEnclosingElement method [Windows Accessibility], GetEnclosingElement method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],GetEnclosingElement method, IUIAutomationTextRange.GetEnclosingElement, IUIAutomationTextRange::GetEnclosingElement, uiauto.uiauto_IUIAutomationTextRange_GetEnclosingElement, uiauto_IUIAutomationTextRange_GetEnclosingElement, uiautomationclient/IUIAutomationTextRange::GetEnclosingElement, winauto.uiauto_IUIAutomationTextRange_GetEnclosingElement
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
 - IUIAutomationTextRange::GetEnclosingElement
 - uiautomationclient/IUIAutomationTextRange::GetEnclosingElement
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
 - IUIAutomationTextRange.GetEnclosingElement
---

# IUIAutomationTextRange::GetEnclosingElement


## -description

Returns the innermost UI Automation element that encloses the text range.

## -parameters

### -param enclosingElement [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the enclosing element, which is typically the text provider that supplies the text range. However, if the text provider supports child elements such as tables or hyperlinks, the enclosing element could be a descendant of the text provider.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>