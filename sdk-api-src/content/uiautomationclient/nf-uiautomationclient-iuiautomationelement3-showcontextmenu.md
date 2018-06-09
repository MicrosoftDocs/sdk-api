---
UID: NF:uiautomationclient.IUIAutomationElement3.ShowContextMenu
title: IUIAutomationElement3::ShowContextMenu
author: windows-sdk-content
description: Programmatically invokes a context menu on the target element.
old-location: winauto\uiauto_IUIAutomationElement3_ShowContextMenu.htm
old-project: WinAuto
ms.assetid: E41A7BE9-2383-EC27-7003-F0EB3CA62103
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IUIAutomationElement3 interface [Windows Accessibility],ShowContextMenu method, IUIAutomationElement3.ShowContextMenu, IUIAutomationElement3::ShowContextMenu, ShowContextMenu, ShowContextMenu method [Windows Accessibility], ShowContextMenu method [Windows Accessibility],IUIAutomationElement3 interface, uiautomationclient/IUIAutomationElement3::ShowContextMenu, winauto.uiauto_IUIAutomationElement3_ShowContextMenu
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
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
 - UIAutomationCore.dll
api_name:
 - IUIAutomationElement3.ShowContextMenu
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationElement3::ShowContextMenu


## -description


Programmatically invokes a context menu on the target element.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method returns   an error code if the context menu could not be invoked. If no context menu is available directly on the element on which it was invoked, calling this method might invoke a context menu on the Microsoft UI Automation parent of the current item.

The context menus themselves fire menu opened / closed events when they are invoked and dismissed.




## -see-also




<a href="https://msdn.microsoft.com/97AB327B-7A5D-C009-F430-42ADFC27F455">IUIAutomationElement3</a>
 

 

