---
UID: NF:uiautomationcore.IRawElementProviderSimple2.ShowContextMenu
title: IRawElementProviderSimple2::ShowContextMenu (uiautomationcore.h)
description: Programmatically invokes a context menu on the target element. (IRawElementProviderSimple2.ShowContextMenu)
helpviewer_keywords: ["IRawElementProviderSimple2 interface [Windows Accessibility]","ShowContextMenu method","IRawElementProviderSimple2.ShowContextMenu","IRawElementProviderSimple2::ShowContextMenu","ShowContextMenu","ShowContextMenu method [Windows Accessibility]","ShowContextMenu method [Windows Accessibility]","IRawElementProviderSimple2 interface","uiautomationcore/IRawElementProviderSimple2::ShowContextMenu","winauto.uiauto_IRawElementProviderSimple2_ShowContextMenu"]
old-location: winauto\uiauto_IRawElementProviderSimple2_ShowContextMenu.htm
tech.root: WinAuto
ms.assetid: DAC75974-4B3E-4C95-F0D7-90D5709EFD93
ms.date: 12/05/2018
ms.keywords: IRawElementProviderSimple2 interface [Windows Accessibility],ShowContextMenu method, IRawElementProviderSimple2.ShowContextMenu, IRawElementProviderSimple2::ShowContextMenu, ShowContextMenu, ShowContextMenu method [Windows Accessibility], ShowContextMenu method [Windows Accessibility],IRawElementProviderSimple2 interface, uiautomationcore/IRawElementProviderSimple2::ShowContextMenu, winauto.uiauto_IRawElementProviderSimple2_ShowContextMenu
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRawElementProviderSimple2::ShowContextMenu
 - uiautomationcore/IRawElementProviderSimple2::ShowContextMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IRawElementProviderSimple2.ShowContextMenu
---

# IRawElementProviderSimple2::ShowContextMenu


## -description

Programmatically invokes a context menu on the target element.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method returns an error code if the context menu could not be invoked.

 If no context menu is available directly on the element on which <b>ShowContextMenu</b> was invoked, the provider should attempt to invoke a context menu on the UI Automation parent of the current item.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple2">IRawElementProviderSimple2</a>
