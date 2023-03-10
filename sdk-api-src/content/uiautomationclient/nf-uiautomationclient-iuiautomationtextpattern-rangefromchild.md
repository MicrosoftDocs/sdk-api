---
UID: NF:uiautomationclient.IUIAutomationTextPattern.RangeFromChild
title: IUIAutomationTextPattern::RangeFromChild (uiautomationclient.h)
description: Retrieves a text range enclosing a child element such as an image, hyperlink, Microsoft Excel spreadsheet, or other embedded object.
helpviewer_keywords: ["IUIAutomationTextPattern interface [Windows Accessibility]","RangeFromChild method","IUIAutomationTextPattern.RangeFromChild","IUIAutomationTextPattern::RangeFromChild","RangeFromChild","RangeFromChild method [Windows Accessibility]","RangeFromChild method [Windows Accessibility]","IUIAutomationTextPattern interface","uiauto.uiauto_IUIAutomationTextPattern_RangeFromChild","uiauto_IUIAutomationTextPattern_RangeFromChild","uiautomationclient/IUIAutomationTextPattern::RangeFromChild","winauto.uiauto_IUIAutomationTextPattern_RangeFromChild"]
old-location: winauto\uiauto_IUIAutomationTextPattern_RangeFromChild.htm
tech.root: WinAuto
ms.assetid: e75d21da-129f-4209-b51b-777ca5880946
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextPattern interface [Windows Accessibility],RangeFromChild method, IUIAutomationTextPattern.RangeFromChild, IUIAutomationTextPattern::RangeFromChild, RangeFromChild, RangeFromChild method [Windows Accessibility], RangeFromChild method [Windows Accessibility],IUIAutomationTextPattern interface, uiauto.uiauto_IUIAutomationTextPattern_RangeFromChild, uiauto_IUIAutomationTextPattern_RangeFromChild, uiautomationclient/IUIAutomationTextPattern::RangeFromChild, winauto.uiauto_IUIAutomationTextPattern_RangeFromChild
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
 - IUIAutomationTextPattern::RangeFromChild
 - uiautomationclient/IUIAutomationTextPattern::RangeFromChild
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
 - IUIAutomationTextPattern.RangeFromChild
---

# IUIAutomationTextPattern::RangeFromChild


## -description

Retrieves a text range enclosing a child element such as an image, hyperlink, Microsoft Excel spreadsheet, or other embedded object.

## -parameters

### -param child [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the child element to be enclosed in the text range.

### -param range [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>**</b>

Receives a pointer to a text range that encloses the child element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If there is no text in the range that encloses the child element, a degenerate (empty) range is returned.

The <i>child</i> parameter is either a child of the element associated with a <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a> or from the array of children of a <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>