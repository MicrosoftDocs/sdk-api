---
UID: NF:uiautomationclient.IUIAutomationLegacyIAccessiblePattern.GetCurrentSelection
title: IUIAutomationLegacyIAccessiblePattern::GetCurrentSelection
author: windows-sdk-content
description: Retrieves the Microsoft Active Accessibility property that identifies the selected children of this element.
old-location: winauto\uiauto_IUIAutomationLegacyIAccessiblePattern_GetCurrentSelection.htm
old-project: WinAuto
ms.assetid: 7fe666dc-2168-44a0-87f2-f444fd2a70f2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetCurrentSelection, GetCurrentSelection method [Windows Accessibility], GetCurrentSelection method [Windows Accessibility],IUIAutomationLegacyIAccessiblePattern interface, IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility],GetCurrentSelection method, IUIAutomationLegacyIAccessiblePattern.GetCurrentSelection, IUIAutomationLegacyIAccessiblePattern::GetCurrentSelection, uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetCurrentSelection, uiauto_IUIAutomationLegacyIAccessiblePattern_GetCurrentSelection, uiautomationclient/IUIAutomationLegacyIAccessiblePattern::GetCurrentSelection, winauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetCurrentSelection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: "*UI_ANIMATION_KEYFRAME"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationLegacyIAccessiblePattern.GetCurrentSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationLegacyIAccessiblePattern::GetCurrentSelection


## -description


Retrieves the Microsoft Active Accessibility property that identifies the selected children of this element.


## -parameters




### -param pvarSelectedChildren [out, retval]

Type: <b><a href="https://msdn.microsoft.com/7ecf585c-ff3b-4f89-8a7d-e2de66650ab4">IUIAutomationElementArray</a>**</b>

Receives a pointer to the collection of the selected child elements.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d6564d14-a739-47bf-9202-0757ac3ba7f8">IUIAutomationLegacyIAccessiblePattern</a>
 

 

