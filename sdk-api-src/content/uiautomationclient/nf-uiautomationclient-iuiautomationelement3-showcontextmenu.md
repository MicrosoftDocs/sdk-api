---
UID: NF:uiautomationclient.IUIAutomationElement3.ShowContextMenu
title: IUIAutomationElement3::ShowContextMenu (uiautomationclient.h)
description: Programmatically invokes a context menu on the target element. (IUIAutomationElement3.ShowContextMenu)
helpviewer_keywords: ["IUIAutomationElement3 interface [Windows Accessibility]","ShowContextMenu method","IUIAutomationElement3.ShowContextMenu","IUIAutomationElement3::ShowContextMenu","ShowContextMenu","ShowContextMenu method [Windows Accessibility]","ShowContextMenu method [Windows Accessibility]","IUIAutomationElement3 interface","uiautomationclient/IUIAutomationElement3::ShowContextMenu","winauto.uiauto_IUIAutomationElement3_ShowContextMenu"]
old-location: winauto\uiauto_IUIAutomationElement3_ShowContextMenu.htm
tech.root: WinAuto
ms.assetid: E41A7BE9-2383-EC27-7003-F0EB3CA62103
ms.date: 12/05/2018
ms.keywords: IUIAutomationElement3 interface [Windows Accessibility],ShowContextMenu method, IUIAutomationElement3.ShowContextMenu, IUIAutomationElement3::ShowContextMenu, ShowContextMenu, ShowContextMenu method [Windows Accessibility], ShowContextMenu method [Windows Accessibility],IUIAutomationElement3 interface, uiautomationclient/IUIAutomationElement3::ShowContextMenu, winauto.uiauto_IUIAutomationElement3_ShowContextMenu
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationElement3::ShowContextMenu
 - uiautomationclient/IUIAutomationElement3::ShowContextMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationElement3.ShowContextMenu
---

# IUIAutomationElement3::ShowContextMenu


## -description

Programmatically invokes a context menu on the target element.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method returns   an error code if the context menu could not be invoked. If no context menu is available directly on the element on which it was invoked, calling this method might invoke a context menu on the Microsoft UI Automation parent of the current item.

The context menus themselves fire menu opened / closed events when they are invoked and dismissed.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement3">IUIAutomationElement3</a>
