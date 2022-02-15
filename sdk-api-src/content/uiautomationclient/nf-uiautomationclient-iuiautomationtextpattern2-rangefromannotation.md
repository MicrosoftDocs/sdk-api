---
UID: NF:uiautomationclient.IUIAutomationTextPattern2.RangeFromAnnotation
title: IUIAutomationTextPattern2::RangeFromAnnotation (uiautomationclient.h)
description: Retrieves a text range containing the text that is the target of the annotation associated with the specified annotation element.
helpviewer_keywords: ["IUIAutomationTextPattern2 interface [Windows Accessibility]","RangeFromAnnotation method","IUIAutomationTextPattern2.RangeFromAnnotation","IUIAutomationTextPattern2::RangeFromAnnotation","RangeFromAnnotation","RangeFromAnnotation method [Windows Accessibility]","RangeFromAnnotation method [Windows Accessibility]","IUIAutomationTextPattern2 interface","uiautomationclient/IUIAutomationTextPattern2::RangeFromAnnotation","winauto.uiauto_iuiautomationtextpattern2_rangefromannotation"]
old-location: winauto\uiauto_iuiautomationtextpattern2_rangefromannotation.htm
tech.root: WinAuto
ms.assetid: C79678D7-2CF4-4DBC-BD0B-7DE22AF25AF9
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextPattern2 interface [Windows Accessibility],RangeFromAnnotation method, IUIAutomationTextPattern2.RangeFromAnnotation, IUIAutomationTextPattern2::RangeFromAnnotation, RangeFromAnnotation, RangeFromAnnotation method [Windows Accessibility], RangeFromAnnotation method [Windows Accessibility],IUIAutomationTextPattern2 interface, uiautomationclient/IUIAutomationTextPattern2::RangeFromAnnotation, winauto.uiauto_iuiautomationtextpattern2_rangefromannotation
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
 - IUIAutomationTextPattern2::RangeFromAnnotation
 - uiautomationclient/IUIAutomationTextPattern2::RangeFromAnnotation
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
 - IUIAutomationTextPattern2.RangeFromAnnotation
---

# IUIAutomationTextPattern2::RangeFromAnnotation


## -description

Retrieves a text range containing the text that is the target of the annotation associated with the specified annotation element.

## -parameters

### -param annotation [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

The annotation element for which to retrieve the target text. This element is a sibling of the element that implements <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern2">IUIAutomationTextPattern2</a> for the document.

### -param range [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>**</b>

Receives a text range that contains the target text of the annotation.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern2">IUIAutomationTextPattern2</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>



<a href="/windows/desktop/WinAuto/uiauto-workingwithtextbasedcontrols">Working with Text-based Controls</a>