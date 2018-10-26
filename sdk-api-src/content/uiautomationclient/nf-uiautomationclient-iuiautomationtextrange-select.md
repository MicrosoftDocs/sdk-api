---
UID: NF:uiautomationclient.IUIAutomationTextRange.Select
title: IUIAutomationTextRange::Select
author: windows-sdk-content
description: Selects the span of text that corresponds to this text range, and removes any previous selection.
old-location: winauto\uiauto_IUIAutomationTextRange_Select.htm
tech.root: WinAuto
ms.assetid: 19e8dfe2-bf58-4ea1-8274-4e914f86ba07
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IUIAutomationTextRange interface [Windows Accessibility],Select method, IUIAutomationTextRange.Select, IUIAutomationTextRange::Select, Select, Select method [Windows Accessibility], Select method [Windows Accessibility],IUIAutomationTextRange interface, uiauto.uiauto_IUIAutomationTextRange_Select, uiauto_IUIAutomationTextRange_Select, uiautomationclient/IUIAutomationTextRange::Select, winauto.uiauto_IUIAutomationTextRange_Select
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
 - IUIAutomationTextRange.Select
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextRange::Select


## -description


Selects the span of text that corresponds to this text range, and removes any previous  selection.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <b>Select</b> method is called on a text range object that represents a degenerate (empty) text range, the text insertion point moves to the starting endpoint of the text range.




## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/5ae4a131-3283-4e91-8419-f2aa6f488833">IUIAutomationTextRange::AddToSelection</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

