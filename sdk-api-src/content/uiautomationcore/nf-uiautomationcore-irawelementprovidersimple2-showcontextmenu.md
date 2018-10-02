---
UID: NF:uiautomationcore.IRawElementProviderSimple2.ShowContextMenu
title: IRawElementProviderSimple2::ShowContextMenu
author: windows-sdk-content
description: Programmatically invokes a context menu on the target element.
old-location: winauto\uiauto_IRawElementProviderSimple2_ShowContextMenu.htm
tech.root: WinAuto
ms.assetid: DAC75974-4B3E-4C95-F0D7-90D5709EFD93
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IRawElementProviderSimple2 interface [Windows Accessibility],ShowContextMenu method, IRawElementProviderSimple2.ShowContextMenu, IRawElementProviderSimple2::ShowContextMenu, ShowContextMenu, ShowContextMenu method [Windows Accessibility], ShowContextMenu method [Windows Accessibility],IRawElementProviderSimple2 interface, uiautomationcore/IRawElementProviderSimple2::ShowContextMenu, winauto.uiauto_IRawElementProviderSimple2_ShowContextMenu
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IRawElementProviderSimple2.ShowContextMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawElementProviderSimple2::ShowContextMenu


## -description


Programmatically invokes a context menu on the target element.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method returns an error code if the context menu could not be invoked.

 If no context menu is available directly on the element on which <b>ShowContextMenu</b> was invoked, the provider should attempt to invoke a context menu on the UI Automation parent of the current item.




## -see-also




<a href="https://msdn.microsoft.com/0B526BDA-CDFA-DDE0-48DC-597D40F1BBB7">IRawElementProviderSimple2</a>
 

 

