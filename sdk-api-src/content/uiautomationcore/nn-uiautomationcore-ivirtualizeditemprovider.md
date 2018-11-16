---
UID: NN:uiautomationcore.IVirtualizedItemProvider
title: IVirtualizedItemProvider
author: windows-sdk-content
description: Provides access to virtualized items, which are items that are represented by placeholder automation elements in the Microsoft UI Automation tree.
old-location: winauto\uiauto_IVirtualizedItemProvider.htm
tech.root: WinAuto
ms.assetid: 39baaa54-b836-497c-b401-a865202626e7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IVirtualizedItemProvider, IVirtualizedItemProvider interface [Windows Accessibility], IVirtualizedItemProvider interface [Windows Accessibility],described, uiauto.uiauto_IVirtualizedItemProvider, uiauto_IVirtualizedItemProvider, uiautomationcore/IVirtualizedItemProvider, winauto.uiauto_IVirtualizedItemProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IVirtualizedItemProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVirtualizedItemProvider interface


## -description


Provides access to virtualized items, which are items that are represented by placeholder automation elements in the Microsoft UI Automation tree.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVirtualizedItemProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVirtualizedItemProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVirtualizedItemProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec69f0d2-a643-4f1b-892a-0d90f79afe72">Realize</a>
</td>
<td align="left" width="63%">
Makes the virtual item fully accessible as a UI Automation element.

</td>
</tr>
</table> 


## -remarks



A virtualized item is typically an item in a virtual list; that is, a list that does not manage its own data. When an application retrieves an <a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a> for a virtualized item by using <a href="https://msdn.microsoft.com/d27f07ae-2c88-4cde-99b8-0c8c987b95d3">FindItemByProperty</a>, UI Automation calls the provider's implementation of <a href="https://msdn.microsoft.com/f2873bbb-5bb4-4eaa-b0bd-60061fc06f53">FindItemByProperty</a>, where the provider may return a placeholder element that also implements <b>IVirtualizedItemProvider</b>. On a call to <a href="https://msdn.microsoft.com/33831b88-cce7-47f3-acd1-e6b74f5a93d2">Realize</a>, the provider's implementation of <a href="https://msdn.microsoft.com/ec69f0d2-a643-4f1b-892a-0d90f79afe72">Realize</a> returns a full UI Automation element reference and may also scroll the item into view.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/7a95e92f-7ccb-4c9b-8986-1d2de7038e47">VirtualizedItem Control Pattern</a>



<a href="https://msdn.microsoft.com/e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52">Working with Virtualized Items</a>
 

 

