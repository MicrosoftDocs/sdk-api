---
UID: NN:uiautomationcore.IRawElementProviderSimple2
title: IRawElementProviderSimple2
author: windows-sdk-content
description: Extends the IRawElementProviderSimple interface to enable programmatically invoking context menus.
old-location: winauto\uiauto_IRawElementProviderSimple2.htm
old-project: WinAuto
ms.assetid: 0B526BDA-CDFA-DDE0-48DC-597D40F1BBB7
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IRawElementProviderSimple2, IRawElementProviderSimple2 interface [Windows Accessibility], IRawElementProviderSimple2 interface [Windows Accessibility],described, uiautomationcore/IRawElementProviderSimple2, winauto.uiauto_IRawElementProviderSimple2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IRawElementProviderSimple2
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRawElementProviderSimple2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a> interface to enable programmatically invoking context menus.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderSimple2</b> interface inherits from <a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>. <b>IRawElementProviderSimple2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRawElementProviderSimple2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DAC75974-4B3E-4C95-F0D7-90D5709EFD93">ShowContextMenu</a>
</td>
<td align="left" width="63%">
Programmatically invokes a context menu on the target element.

</td>
</tr>
</table> 


## -remarks



This interface can be implemented on:
			

<ul>
<li>Providers that add or override properties or control patterns on a UI element that already has a provider.</li>
</ul>
 If no context menu is available directly on the element on which <a href="https://msdn.microsoft.com/DAC75974-4B3E-4C95-F0D7-90D5709EFD93">ShowContextMenu</a>  was invoked, the provider should attempt to invoke a context menu on the UI Automation parent of the current item.



