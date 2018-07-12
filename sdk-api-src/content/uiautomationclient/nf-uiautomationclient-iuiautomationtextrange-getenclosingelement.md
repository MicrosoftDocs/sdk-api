---
UID: NF:uiautomationclient.IUIAutomationTextRange.GetEnclosingElement
title: IUIAutomationTextRange::GetEnclosingElement
author: windows-sdk-content
description: Returns the innermost UI Automation element that encloses the text range.
old-location: winauto\uiauto_IUIAutomationTextRange_GetEnclosingElement.htm
old-project: WinAuto
ms.assetid: 0120b4af-6f08-4bbd-b649-0f8e84cda3b9
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetEnclosingElement, GetEnclosingElement method [Windows Accessibility], GetEnclosingElement method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],GetEnclosingElement method, IUIAutomationTextRange.GetEnclosingElement, IUIAutomationTextRange::GetEnclosingElement, uiauto.uiauto_IUIAutomationTextRange_GetEnclosingElement, uiauto_IUIAutomationTextRange_GetEnclosingElement, uiautomationclient/IUIAutomationTextRange::GetEnclosingElement, winauto.uiauto_IUIAutomationTextRange_GetEnclosingElement
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTextRange.GetEnclosingElement
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTextRange::GetEnclosingElement


## -description


Returns the innermost UI Automation element that encloses the text range.


## -parameters




### -param enclosingElement [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the enclosing element, which is typically the text provider that supplies the text range. However, if the text provider supports child elements such as tables or hyperlinks, the enclosing element could be a descendant of the text provider.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

