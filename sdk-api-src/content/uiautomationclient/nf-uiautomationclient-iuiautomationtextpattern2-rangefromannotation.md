---
UID: NF:uiautomationclient.IUIAutomationTextPattern2.RangeFromAnnotation
title: IUIAutomationTextPattern2::RangeFromAnnotation
author: windows-sdk-content
description: Retrieves a text range containing the text that is the target of the annotation associated with the specified annotation element.
old-location: winauto\uiauto_iuiautomationtextpattern2_rangefromannotation.htm
tech.root: WinAuto
ms.assetid: C79678D7-2CF4-4DBC-BD0B-7DE22AF25AF9
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IUIAutomationTextPattern2 interface [Windows Accessibility],RangeFromAnnotation method, IUIAutomationTextPattern2.RangeFromAnnotation, IUIAutomationTextPattern2::RangeFromAnnotation, RangeFromAnnotation, RangeFromAnnotation method [Windows Accessibility], RangeFromAnnotation method [Windows Accessibility],IUIAutomationTextPattern2 interface, uiautomationclient/IUIAutomationTextPattern2::RangeFromAnnotation, winauto.uiauto_iuiautomationtextpattern2_rangefromannotation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTextPattern2.RangeFromAnnotation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextPattern2::RangeFromAnnotation


## -description


Retrieves a text range containing the text that is the target of the annotation associated with the specified annotation element.


## -parameters




### -param annotation [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

The annotation element for which to retrieve the target text. This element is a sibling of the element that implements <a href="https://msdn.microsoft.com/E7160CDD-9A83-42F9-9F7B-8A8C13849E20">IUIAutomationTextPattern2</a> for the document.


### -param range [out, retval]

Type: <b><a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>**</b>

Receives a text range that contains the target text of the annotation. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/E7160CDD-9A83-42F9-9F7B-8A8C13849E20">IUIAutomationTextPattern2</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>



<a href="https://msdn.microsoft.com/e06e1f6e-8346-4656-b0cb-58e5b9fdaa33">Working with Text-based Controls</a>
 

 

