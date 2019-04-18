---
UID: NF:uiautomationclient.IUIAutomationTextPattern.RangeFromPoint
title: IUIAutomationTextPattern::RangeFromPoint (uiautomationclient.h)
author: windows-sdk-content
description: Retrieves the degenerate (empty) text range nearest to the specified screen coordinates.
old-location: winauto\uiauto_IUIAutomationTextPattern_RangeFromPoint.htm
tech.root: WinAuto
ms.assetid: aa80b1d8-c50e-45be-8769-8b937c8e714a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextPattern interface [Windows Accessibility],RangeFromPoint method, IUIAutomationTextPattern.RangeFromPoint, IUIAutomationTextPattern::RangeFromPoint, RangeFromPoint, RangeFromPoint method [Windows Accessibility], RangeFromPoint method [Windows Accessibility],IUIAutomationTextPattern interface, uiauto.uiauto_IUIAutomationTextPattern_RangeFromPoint, uiauto_IUIAutomationTextPattern_RangeFromPoint, uiautomationclient/IUIAutomationTextPattern::RangeFromPoint, winauto.uiauto_IUIAutomationTextPattern_RangeFromPoint
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTextPattern.RangeFromPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTextPattern::RangeFromPoint


## -description


Retrieves the degenerate (empty) text range nearest to the specified screen coordinates.


## -parameters




### -param pt [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

A structure that contains the location, in screen coordinates.


### -param range [out, retval]

Type: <b><a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>**</b>

Receives a pointer to the degenerate text range nearest the specified location.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A text range that wraps a child object is returned if the screen coordinates are within the coordinates of an image, hyperlink, Microsoft Excel spreadsheet, or other embedded object.

Because hidden text is not ignored, this method retrieves a degenerate range from the visible text closest to the specified coordinates.

The implementation of <b>RangeFromPoint</b> in Windows Internet Explorer 9 does not return the expected result. Instead, clients should:

<ol>
<li>Call the <a href="https://msdn.microsoft.com/7cf4e6d4-223c-4222-a181-c16a5a90ef65">GetVisibleRanges</a> method to retrieve an array of visible text ranges.</li>
<li>For each text range in the array, call <a href="https://msdn.microsoft.com/a155d143-c5ec-4669-9635-fb8f8012a684">IUIAutomationTextRange::GetBoundingRectangles</a> to retrieve the bounding rectangles.</li>
<li>Check the bounding rectangles to find the text range that occupies the particular screen coordinates. </li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/ddcf7ecd-7ed2-4b57-82a7-c7e1608dbfa1">IUIAutomationTextPattern</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

