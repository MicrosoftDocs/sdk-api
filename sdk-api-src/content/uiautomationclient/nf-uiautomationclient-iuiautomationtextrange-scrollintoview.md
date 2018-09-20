---
UID: NF:uiautomationclient.IUIAutomationTextRange.ScrollIntoView
title: IUIAutomationTextRange::ScrollIntoView
author: windows-sdk-content
description: Causes the text control to scroll until the text range is visible in the viewport.
old-location: winauto\uiauto_IUIAutomationTextRange_ScrollIntoView.htm
tech.root: WinAuto
ms.assetid: 0d1ec553-1cc2-4b1c-a393-2507a3756a6c
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IUIAutomationTextRange interface [Windows Accessibility],ScrollIntoView method, IUIAutomationTextRange.ScrollIntoView, IUIAutomationTextRange::ScrollIntoView, ScrollIntoView, ScrollIntoView method [Windows Accessibility], ScrollIntoView method [Windows Accessibility],IUIAutomationTextRange interface, uiauto.uiauto_IUIAutomationTextRange_ScrollIntoView, uiauto_IUIAutomationTextRange_ScrollIntoView, uiautomationclient/IUIAutomationTextRange::ScrollIntoView, winauto.uiauto_IUIAutomationTextRange_ScrollIntoView
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
 - IUIAutomationTextRange.ScrollIntoView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextRange::ScrollIntoView


## -description


Causes the text control to scroll until the text range is visible in the viewport.


## -parameters




### -param alignToTop [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the text control should be scrolled so that the text range is flush with the top of the viewport; <b>FALSE</b> if it should be flush with the bottom of the viewport.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The method respects both hidden and visible text. If the text range is hidden, the text control will scroll only if the hidden text has an anchor in the viewport. 

 A Microsoft UI Automation client can check text visibility by calling <a href="https://msdn.microsoft.com/7a77774e-7be0-473e-a0c9-e1aa108549e1">IUIAutomationTextRange::GetAttributeValue</a> with the <i>attr</i> parameter set to <a href="uiauto_textattribute_ids.htm">UIA_IsHiddenAttributeId</a>.  




## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

