---
UID: NF:uiautomationclient.IUIAutomationTextPattern.GetVisibleRanges
title: IUIAutomationTextPattern::GetVisibleRanges (uiautomationclient.h)
description: Retrieves an array of disjoint text ranges from a text-based control where each text range represents a contiguous span of visible text. (IUIAutomationTextPattern.GetVisibleRanges)
helpviewer_keywords: ["GetVisibleRanges","GetVisibleRanges method [Windows Accessibility]","GetVisibleRanges method [Windows Accessibility]","IUIAutomationTextPattern interface","IUIAutomationTextPattern interface [Windows Accessibility]","GetVisibleRanges method","IUIAutomationTextPattern.GetVisibleRanges","IUIAutomationTextPattern::GetVisibleRanges","uiauto.uiauto_IUIAutomationTextPattern_GetVisibleRanges","uiauto_IUIAutomationTextPattern_GetVisibleRanges","uiautomationclient/IUIAutomationTextPattern::GetVisibleRanges","winauto.uiauto_IUIAutomationTextPattern_GetVisibleRanges"]
old-location: winauto\uiauto_IUIAutomationTextPattern_GetVisibleRanges.htm
tech.root: WinAuto
ms.assetid: 7cf4e6d4-223c-4222-a181-c16a5a90ef65
ms.date: 12/05/2018
ms.keywords: GetVisibleRanges, GetVisibleRanges method [Windows Accessibility], GetVisibleRanges method [Windows Accessibility],IUIAutomationTextPattern interface, IUIAutomationTextPattern interface [Windows Accessibility],GetVisibleRanges method, IUIAutomationTextPattern.GetVisibleRanges, IUIAutomationTextPattern::GetVisibleRanges, uiauto.uiauto_IUIAutomationTextPattern_GetVisibleRanges, uiauto_IUIAutomationTextPattern_GetVisibleRanges, uiautomationclient/IUIAutomationTextPattern::GetVisibleRanges, winauto.uiauto_IUIAutomationTextPattern_GetVisibleRanges
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
 - IUIAutomationTextPattern::GetVisibleRanges
 - uiautomationclient/IUIAutomationTextPattern::GetVisibleRanges
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
 - IUIAutomationTextPattern.GetVisibleRanges
---

# IUIAutomationTextPattern::GetVisibleRanges


## -description

Retrieves an array of disjoint text ranges from a text-based control where each text range represents a contiguous span of visible text.

## -parameters

### -param ranges [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrangearray">IUIAutomationTextRangeArray</a>**</b>

Receives a pointer to the collection of visible text ranges within the text-based control.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the visible text consists of one contiguous span of text, the <i>ranges</i> array will contain a single text range that represents all of the visible text. 

If the visible text consists of multiple, disjoint spans of text, the <i>ranges</i> array will contain one text range for each visible span, beginning with the first visible span, and ending with the last visible span. Disjoint spans of visible text can occur when the content of a text-based control is partially obscured 
            by an overlapping window or other object, or when a text-based  control with multiple pages or columns 
            has content that is partially scrolled out of view.
            

<b>IUIAutomationTextPattern::GetVisibleRanges</b> retrieves  a degenerate (empty) text range if no text is visible, if all text is scrolled out of view, or if the text-based control contains no text.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>
