---
UID: NF:uiautomationclient.IUIAutomationTextRange2.ShowContextMenu
title: IUIAutomationTextRange2::ShowContextMenu (uiautomationclient.h)
description: Programmatically invokes a context menu on the target text range.
helpviewer_keywords: ["IUIAutomationTextRange2 interface [Windows Accessibility]","ShowContextMenu method","IUIAutomationTextRange2.ShowContextMenu","IUIAutomationTextRange2::ShowContextMenu","ShowContextMenu","ShowContextMenu method [Windows Accessibility]","ShowContextMenu method [Windows Accessibility]","IUIAutomationTextRange2 interface","uiautomationclient/IUIAutomationTextRange2::ShowContextMenu","winauto.uiauto_IUIAutomationTextRange2_ShowContextMenu"]
old-location: winauto\uiauto_IUIAutomationTextRange2_ShowContextMenu.htm
tech.root: WinAuto
ms.assetid: 03165205-C56C-6002-A820-9214725B93E1
ms.date: 12/05/2018
ms.keywords: IUIAutomationTextRange2 interface [Windows Accessibility],ShowContextMenu method, IUIAutomationTextRange2.ShowContextMenu, IUIAutomationTextRange2::ShowContextMenu, ShowContextMenu, ShowContextMenu method [Windows Accessibility], ShowContextMenu method [Windows Accessibility],IUIAutomationTextRange2 interface, uiautomationclient/IUIAutomationTextRange2::ShowContextMenu, winauto.uiauto_IUIAutomationTextRange2_ShowContextMenu
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
 - IUIAutomationTextRange2::ShowContextMenu
 - uiautomationclient/IUIAutomationTextRange2::ShowContextMenu
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
 - IUIAutomationTextRange2.ShowContextMenu
---

# IUIAutomationTextRange2::ShowContextMenu


## -description

Programmatically invokes a context menu on the target text range.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method returns an error code if the context menu could not be invoked. If no context menu is available directly on the text range on which it was invoked, the Microsoft UI Automation system might attempt to invoke a context menu on the UI Automation parent of the current item.

The context menus themselves fire menu opened / closed events when they are invoked and dismissed.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange2">IUIAutomationTextRange2</a>



<a href="/windows/desktop/WinAuto/uiauto-usingtextrangeobjects">Using Text Ranges</a>
