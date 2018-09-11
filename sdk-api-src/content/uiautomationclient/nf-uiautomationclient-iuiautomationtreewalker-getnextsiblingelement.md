---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.GetNextSiblingElement
title: IUIAutomationTreeWalker::GetNextSiblingElement
author: windows-sdk-content
description: Retrieves the next sibling element of the specified UI Automation element, and caches properties and control patterns.
old-location: winauto\uiauto_IUIAutomationTreeWalker_GetNextSibling.htm
tech.root: WinAuto
ms.assetid: a1e42cb4-0b87-42c2-9ea5-67630c0b895a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetNextSiblingElement, GetNextSiblingElement method [Windows Accessibility], GetNextSiblingElement method [Windows Accessibility],IUIAutomationTreeWalker interface, IUIAutomationTreeWalker interface [Windows Accessibility],GetNextSiblingElement method, IUIAutomationTreeWalker.GetNextSiblingElement, IUIAutomationTreeWalker::GetNextSiblingElement, uiauto.uiauto_IUIAutomationTreeWalker_GetNextSibling, uiauto_IUIAutomationTreeWalker_GetNextSibling, uiautomationclient/IUIAutomationTreeWalker::GetNextSiblingElement, winauto.uiauto_IUIAutomationTreeWalker_GetNextSibling
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
 - IUIAutomationTreeWalker.GetNextSiblingElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTreeWalker::GetNextSiblingElement


## -description


Retrieves the next sibling element of the specified UI Automation element, and caches properties and control patterns.


## -parameters




### -param element [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the element for which to retrieve the next sibling.


### -param next [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the next sibling element, or <b>NULL</b> if there is no sibling element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An element can have additional sibling elements that do not match the current view condition and thus are not returned when navigating the element tree.

The structure of the Microsoft UI Automation tree changes as the visible UI elements on the desktop change. It is not guaranteed that an element returned as the next sibling element will be returned as the next sibling on subsequent passes.



