---
UID: NF:uiautomationclient.IUIAutomationElement.GetCachedPattern
title: IUIAutomationElement::GetCachedPattern
author: windows-sdk-content
description: Retrieves from the cache the IUnknown interface of the specified control pattern of this UI Automation element.
old-location: winauto\uiauto_IUIAutomationElement_GetCachedPattern.htm
tech.root: WinAuto
ms.assetid: c71cab11-24c7-4e66-bcf2-f1abb1f37abb
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetCachedPattern, GetCachedPattern method [Windows Accessibility], GetCachedPattern method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCachedPattern method, IUIAutomationElement.GetCachedPattern, IUIAutomationElement::GetCachedPattern, uiauto.uiauto_IUIAutomationElement_GetCachedPattern, uiauto_IUIAutomationElement_GetCachedPattern, uiautomationclient/IUIAutomationElement::GetCachedPattern, winauto.uiauto_IUIAutomationElement_GetCachedPattern
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
 - IUIAutomationElement.GetCachedPattern
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationElement::GetCachedPattern


## -description


Retrieves from the cache the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the specified control pattern of this UI Automation element. 


## -parameters




### -param patternId [in]

Type: <b>PATTERNID</b>

The identifier of the control pattern. For a list of control pattern IDs, see <a href="https://msdn.microsoft.com/0192e840-96e6-4b12-a570-0d33a36ed885">Control Pattern Identifiers</a>.


### -param patternObject [out, retval]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

Receives a pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/2d0170e2-277e-48f8-a2e4-5c4ece92d8ec">GetCachedPatternAs</a>



<a href="https://msdn.microsoft.com/3ad4df7c-979d-464f-9600-d1f3de064b59">GetCurrentPattern</a>



<a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/fdac2b9f-916a-495a-b187-c4d8086319ff">UI Automation Control Patterns Overview</a>
 

 

