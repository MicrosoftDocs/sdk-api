---
UID: NN:uiautomationcore.IRawElementProviderSimple2
title: IRawElementProviderSimple2 (uiautomationcore.h)
description: Extends the IRawElementProviderSimple interface to enable programmatically invoking context menus.
helpviewer_keywords: ["IRawElementProviderSimple2","IRawElementProviderSimple2 interface [Windows Accessibility]","IRawElementProviderSimple2 interface [Windows Accessibility]","described","uiautomationcore/IRawElementProviderSimple2","winauto.uiauto_IRawElementProviderSimple2"]
old-location: winauto\uiauto_IRawElementProviderSimple2.htm
tech.root: WinAuto
ms.assetid: 0B526BDA-CDFA-DDE0-48DC-597D40F1BBB7
ms.date: 12/05/2018
ms.keywords: IRawElementProviderSimple2, IRawElementProviderSimple2 interface [Windows Accessibility], IRawElementProviderSimple2 interface [Windows Accessibility],described, uiautomationcore/IRawElementProviderSimple2, winauto.uiauto_IRawElementProviderSimple2
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
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRawElementProviderSimple2
 - uiautomationcore/IRawElementProviderSimple2
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
 - IRawElementProviderSimple2
---

# IRawElementProviderSimple2 interface


## -description

Extends the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a> interface to enable programmatically invoking context menus.

## -inheritance

The <b>IRawElementProviderSimple2</b> interface inherits from <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>. <b>IRawElementProviderSimple2</b> also has these types of members:

## -remarks

This interface can be implemented on:
			

<ul>
<li>Providers that add or override properties or control patterns on a UI element that already has a provider.</li>
</ul>
 If no context menu is available directly on the element on which <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementprovidersimple2-showcontextmenu">ShowContextMenu</a>  was invoked, the provider should attempt to invoke a context menu on the UI Automation parent of the current item.
