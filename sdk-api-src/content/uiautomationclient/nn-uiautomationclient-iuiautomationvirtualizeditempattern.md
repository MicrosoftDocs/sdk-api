---
UID: NN:uiautomationclient.IUIAutomationVirtualizedItemPattern
title: IUIAutomationVirtualizedItemPattern
author: windows-sdk-content
description: Represents an virtualized item, which is an item that is represented by a placeholder automation element in the Microsoft UI Automation tree.
old-location: winauto\uiauto_IUIAutomationVirtualizedItemPattern.htm
old-project: WinAuto
ms.assetid: 48f066f3-c78c-47a2-9668-ab79b1438130
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: IUIAutomationVirtualizedItemPattern, IUIAutomationVirtualizedItemPattern interface [Windows Accessibility], IUIAutomationVirtualizedItemPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationVirtualizedItemPattern, uiauto_IUIAutomationVirtualizedItemPattern, uiautomationclient/IUIAutomationVirtualizedItemPattern, winauto.uiauto_IUIAutomationVirtualizedItemPattern
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.dll
api_name:
-	IUIAutomationVirtualizedItemPattern
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationVirtualizedItemPattern interface


## -description


Represents an virtualized item, which is an item that is represented by a placeholder automation element in the Microsoft UI Automation tree.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationVirtualizedItemPattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationVirtualizedItemPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAutomationVirtualizedItemPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33831b88-cce7-47f3-acd1-e6b74f5a93d2">Realize</a>
</td>
<td align="left" width="63%">
Creates a full UI Automation element for a virtualized item.

</td>
</tr>
</table> 


## -remarks



A virtualized item can be an item retrieved from a control that supports the <a href="https://msdn.microsoft.com/6f3dd94e-3563-4a13-9db9-5928a02bab77">ItemContainer</a> control pattern, or a virtualized embedded object retrieved from a control that supports the <a href="https://msdn.microsoft.com/acc2b513-9367-416a-b0d9-3c2bcc14a8a7">Text</a> control pattern.

The placeholder automation element for a virtualized item might not have loaded data for all UI Automation properties, and may return <a href="uiauto_error_codes.htm">UIA_E_ELEMENTNOTAVAILABLE</a> in response to queries for properties that are not available.




## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>



<a href="https://msdn.microsoft.com/e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52">Working with Virtualized Items</a>
 

 

