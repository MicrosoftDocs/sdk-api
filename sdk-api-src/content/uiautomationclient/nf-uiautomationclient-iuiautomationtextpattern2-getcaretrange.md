---
UID: NF:uiautomationclient.IUIAutomationTextPattern2.GetCaretRange
title: IUIAutomationTextPattern2::GetCaretRange
author: windows-sdk-content
description: Retrieves a zero-length text range at the location of the caret that belongs to the text-based control.
old-location: winauto\uiauto_IUIAutomationTextPattern2_GetCaretRange.htm
tech.root: WinAuto
ms.assetid: EDB53C04-142E-4DCC-8DD7-F7DD4BC6A67F
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetCaretRange, GetCaretRange method [Windows Accessibility], GetCaretRange method [Windows Accessibility],IUIAutomationTextPattern2 interface, IUIAutomationTextPattern2 interface [Windows Accessibility],GetCaretRange method, IUIAutomationTextPattern2.GetCaretRange, IUIAutomationTextPattern2::GetCaretRange, uiautomationclient/IUIAutomationTextPattern2::GetCaretRange, winauto.uiauto_IUIAutomationTextPattern2_GetCaretRange
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
 - IUIAutomationTextPattern2.GetCaretRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextPattern2::GetCaretRange


## -description


Retrieves a zero-length text range at the location of the caret that belongs to the text-based control.


## -parameters




### -param isActive [out, retval]

Type: <b>BOOL*</b>

<b>TRUE</b> if the text-based control that contains the caret has keyboard focus, otherwise <b>FALSE</b>.


### -param range

TBD




#### - ppRange [out, retval]

Type: <b><a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>**</b>

Receives a text range that represents the current location of the caret that belongs to the text-based control. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <i>isActive</i> parameter is <b>FALSE</b>, the caret that belongs to the text-based control might not be at the same location as the system caret.

This method retrieves a text range that a client can use to find the bounding rectangle of the caret belonging to the text-based control, or to find the text near the caret.




## -see-also




<a href="https://msdn.microsoft.com/E7160CDD-9A83-42F9-9F7B-8A8C13849E20">IUIAutomationTextPattern2</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>



<a href="https://msdn.microsoft.com/e06e1f6e-8346-4656-b0cb-58e5b9fdaa33">Working with Text-based Controls</a>
 

 

