---
UID: NF:uiautomationclient.IUIAutomationTextRange.RemoveFromSelection
title: IUIAutomationTextRange::RemoveFromSelection
author: windows-sdk-content
description: Removes the text range from an existing collection of selected text in a text container that supports multiple, disjoint selections.
old-location: winauto\uiauto_IUIAutomationTextRange_RemoveFromSelection.htm
tech.root: WinAuto
ms.assetid: 24aa2e4f-4024-4915-81f5-4bc704cc1559
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAutomationTextRange interface [Windows Accessibility],RemoveFromSelection method, IUIAutomationTextRange.RemoveFromSelection, IUIAutomationTextRange::RemoveFromSelection, RemoveFromSelection, RemoveFromSelection method [Windows Accessibility], RemoveFromSelection method [Windows Accessibility],IUIAutomationTextRange interface, uiauto.uiauto_IUIAutomationTextRange_RemoveFromSelection, uiauto_IUIAutomationTextRange_RemoveFromSelection, uiautomationclient/IUIAutomationTextRange::RemoveFromSelection, winauto.uiauto_IUIAutomationTextRange_RemoveFromSelection
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
 - IUIAutomationTextRange.RemoveFromSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextRange::RemoveFromSelection


## -description


Removes the text range from an existing collection of selected text in a text container that supports multiple, disjoint selections.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The text insertion point moves to the area of the removed highlight. Providing a degenerate text range also moves the insertion point.




## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

