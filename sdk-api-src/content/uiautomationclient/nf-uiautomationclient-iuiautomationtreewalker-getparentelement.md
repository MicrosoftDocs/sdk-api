---
UID: NF:uiautomationclient.IUIAutomationTreeWalker.GetParentElement
title: IUIAutomationTreeWalker::GetParentElement
author: windows-sdk-content
description: Retrieves the parent element of the specified UI Automation element.
old-location: winauto\uiauto_IUIAutomationTreeWalker_GetParent.htm
tech.root: WinAuto
ms.assetid: eaff4d83-a614-4559-a357-dc2d241ecf67
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetParentElement, GetParentElement method [Windows Accessibility], GetParentElement method [Windows Accessibility],IUIAutomationTreeWalker interface, IUIAutomationTreeWalker interface [Windows Accessibility],GetParentElement method, IUIAutomationTreeWalker.GetParentElement, IUIAutomationTreeWalker::GetParentElement, uiauto.uiauto_IUIAutomationTreeWalker_GetParent, uiauto_IUIAutomationTreeWalker_GetParent, uiautomationclient/IUIAutomationTreeWalker::GetParentElement, winauto.uiauto_IUIAutomationTreeWalker_GetParent
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
 - IUIAutomationTreeWalker.GetParentElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTreeWalker::GetParentElement


## -description


Retrieves the parent element of the specified UI Automation element.


## -parameters




### -param element [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the element for which to retrieve the parent.


### -param parent [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the parent element, or <b>NULL</b> if there is no parent element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The structure of the Microsoft UI Automation tree changes as the visible UI elements on the desktop change. It is not guaranteed that an element returned as the  parent element will be returned as the parent on subsequent passes.



