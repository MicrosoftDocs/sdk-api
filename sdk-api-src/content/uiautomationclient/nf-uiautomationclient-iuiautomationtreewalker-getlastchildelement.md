---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.GetLastChildElement
title: IUIAutomationTreeWalker::GetLastChildElement
author: windows-sdk-content
description: Retrieves the last child element of the specified UI Automation element.
old-location: winauto\uiauto_IUIAutomationTreeWalker_GetLastChild.htm
tech.root: WinAuto
ms.assetid: 9e59d8f6-1540-4077-9e0e-f75bf8846da9
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: GetLastChildElement, GetLastChildElement method [Windows Accessibility], GetLastChildElement method [Windows Accessibility],IUIAutomationTreeWalker interface, IUIAutomationTreeWalker interface [Windows Accessibility],GetLastChildElement method, IUIAutomationTreeWalker.GetLastChildElement, IUIAutomationTreeWalker::GetLastChildElement, uiauto.uiauto_IUIAutomationTreeWalker_GetLastChild, uiauto_IUIAutomationTreeWalker_GetLastChild, uiautomationclient/IUIAutomationTreeWalker::GetLastChildElement, winauto.uiauto_IUIAutomationTreeWalker_GetLastChild
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
 - IUIAutomationTreeWalker.GetLastChildElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTreeWalker::GetLastChildElement


## -description


Retrieves the last child element of the specified UI Automation element.


## -parameters




### -param element [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to  the element for which to retrieve the last child.


### -param last [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the last child element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An element can have additional child elements that do not match the current view condition and thus are not returned when navigating the element tree.

The structure of the Microsoft UI Automation tree changes as the visible UI elements on the desktop change. It is not guaranteed that an element returned as the last child element will be returned as the last child on subsequent passes.



