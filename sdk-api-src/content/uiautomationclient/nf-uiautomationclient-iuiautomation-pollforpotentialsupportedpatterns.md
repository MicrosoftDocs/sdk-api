---
UID: NF:uiautomationclient.IUIAutomation.PollForPotentialSupportedPatterns
title: IUIAutomation::PollForPotentialSupportedPatterns
author: windows-sdk-content
description: Retrieves the control patterns that might be supported on a UI Automation element.
old-location: winauto\uiauto_IUIAutomation_PollForPotentialSupportedPatterns.htm
tech.root: WinAuto
ms.assetid: 1319420e-17d6-4d0f-81c5-46b22b644e68
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],PollForPotentialSupportedPatterns method, IUIAutomation.PollForPotentialSupportedPatterns, IUIAutomation::PollForPotentialSupportedPatterns, PollForPotentialSupportedPatterns, PollForPotentialSupportedPatterns method [Windows Accessibility], PollForPotentialSupportedPatterns method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_PollForPotentialSupportedPatterns, uiauto_IUIAutomation_PollForPotentialSupportedPatterns, uiautomationclient/IUIAutomation::PollForPotentialSupportedPatterns, winauto.uiauto_IUIAutomation_PollForPotentialSupportedPatterns
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
 - IUIAutomation.PollForPotentialSupportedPatterns
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::PollForPotentialSupportedPatterns


## -description


Retrieves the control patterns that might be supported on a UI Automation element.


## -parameters




### -param pElement [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

The address of the element to poll.


### -param patternIds [out]

Type: <b>SAFEARRAY(int)**</b>

Receives a pointer to an array of control pattern identifiers.


### -param patternNames [out]

Type: <b>SAFEARRAY(BSTR)**</b>

Receives a pointer to an array of control pattern names.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is intended only for use by Microsoft UI Automation tools that need to scan for properties. It is not intended to be used by UI Automation clients.

There is no guarantee that the element will support any particular control pattern when asked for it later.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d1eca598-1a02-4437-8036-77c8d62032d5">Custom Properties, Events, and Control Patterns</a>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<a href="https://msdn.microsoft.com/2cb78604-3c61-4362-9d8a-e40d5ddb4047">PollForPotentialSupportedProperties</a>



<b>Reference</b>
 

 

