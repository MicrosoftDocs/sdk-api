---
UID: NF:uiautomationclient.IUIAutomationTextPattern.RangeFromPoint
title: IUIAutomationTextPattern::RangeFromPoint (uiautomationclient.h)
description: Retrieves the degenerate (empty) text range nearest to the specified screen coordinates. (IUIAutomationTextPattern.RangeFromPoint)
helpviewer_keywords: ["IUIAutomationTextPattern interface [Windows Accessibility]","RangeFromPoint method","IUIAutomationTextPattern.RangeFromPoint","IUIAutomationTextPattern::RangeFromPoint","RangeFromPoint","RangeFromPoint method [Windows Accessibility]","RangeFromPoint method [Windows Accessibility]","IUIAutomationTextPattern interface","uiauto.uiauto_IUIAutomationTextPattern_RangeFromPoint","uiauto_IUIAutomationTextPattern_RangeFromPoint","uiautomationclient/IUIAutomationTextPattern::RangeFromPoint","winauto.uiauto_IUIAutomationTextPattern_RangeFromPoint"]
old-location: winauto\uiauto_IUIAutomationTextPattern_RangeFromPoint.htm
tech.root: WinAuto
ms.assetid: aa80b1d8-c50e-45be-8769-8b937c8e714a
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextPattern interface [Windows Accessibility],RangeFromPoint method, IUIAutomationTextPattern.RangeFromPoint, IUIAutomationTextPattern::RangeFromPoint, RangeFromPoint, RangeFromPoint method [Windows Accessibility], RangeFromPoint method [Windows Accessibility],IUIAutomationTextPattern interface, uiauto.uiauto_IUIAutomationTextPattern_RangeFromPoint, uiauto_IUIAutomationTextPattern_RangeFromPoint, uiautomationclient/IUIAutomationTextPattern::RangeFromPoint, winauto.uiauto_IUIAutomationTextPattern_RangeFromPoint
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
 - IUIAutomationTextPattern::RangeFromPoint
 - uiautomationclient/IUIAutomationTextPattern::RangeFromPoint
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
 - IUIAutomationTextPattern.RangeFromPoint
---

# IUIAutomationTextPattern::RangeFromPoint


## -description

Retrieves the degenerate (empty) text range nearest to the specified screen coordinates.

## -parameters

### -param pt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

A structure that contains the location, in screen coordinates.

### -param range [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>**</b>

Receives a pointer to the degenerate text range nearest the specified location.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A text range that wraps a child object is returned if the screen coordinates are within the coordinates of an image, hyperlink, Microsoft Excel spreadsheet, or other embedded object.

Because hidden text is not ignored, this method retrieves a degenerate range from the visible text closest to the specified coordinates.

The implementation of <b>RangeFromPoint</b> in Windows Internet Explorer 9 does not return the expected result. Instead, clients should:

<ol>
<li>Call the <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextpattern-getvisibleranges">GetVisibleRanges</a> method to retrieve an array of visible text ranges.</li>
<li>For each text range in the array, call <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtextrange-getboundingrectangles">IUIAutomationTextRange::GetBoundingRectangles</a> to retrieve the bounding rectangles.</li>
<li>Check the bounding rectangles to find the text range that occupies the particular screen coordinates. </li>
</ol>

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>
