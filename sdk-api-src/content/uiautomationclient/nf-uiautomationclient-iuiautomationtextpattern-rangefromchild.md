---
UID: NF:uiautomationclient.IUIAutomationTextPattern.RangeFromChild
title: IUIAutomationTextPattern::RangeFromChild
author: windows-sdk-content
description: Retrieves a text range enclosing a child element such as an image, hyperlink, Microsoft Excel spreadsheet, or other embedded object.
old-location: winauto\uiauto_IUIAutomationTextPattern_RangeFromChild.htm
tech.root: WinAuto
ms.assetid: e75d21da-129f-4209-b51b-777ca5880946
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: IUIAutomationTextPattern interface [Windows Accessibility],RangeFromChild method, IUIAutomationTextPattern.RangeFromChild, IUIAutomationTextPattern::RangeFromChild, RangeFromChild, RangeFromChild method [Windows Accessibility], RangeFromChild method [Windows Accessibility],IUIAutomationTextPattern interface, uiauto.uiauto_IUIAutomationTextPattern_RangeFromChild, uiauto_IUIAutomationTextPattern_RangeFromChild, uiautomationclient/IUIAutomationTextPattern::RangeFromChild, winauto.uiauto_IUIAutomationTextPattern_RangeFromChild
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IUIAutomationTextPattern.RangeFromChild
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextPattern::RangeFromChild


## -description


Retrieves a text range enclosing a child element such as an image, hyperlink, Microsoft Excel spreadsheet, or other embedded object.


## -parameters




### -param child [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the child element to be enclosed in the text range.


### -param range [out, retval]

Type: <b><a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>**</b>

Receives a pointer to a text range that encloses the child element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If there is no text in the range that encloses the child element, a degenerate (empty) range is returned.

The <i>child</i> parameter is either a child of the element associated with a <a href="https://msdn.microsoft.com/ddcf7ecd-7ed2-4b57-82a7-c7e1608dbfa1">IUIAutomationTextPattern</a> or from the array of children of a <a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>.




## -see-also




<a href="https://msdn.microsoft.com/ddcf7ecd-7ed2-4b57-82a7-c7e1608dbfa1">IUIAutomationTextPattern</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

