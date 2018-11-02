---
UID: NN:uiautomationclient.IUIAutomationElement3
title: IUIAutomationElement3
author: windows-sdk-content
description: Extends the IUIAutomationElement2 interface.
old-location: winauto\uiauto_IUIAutomationElement3.htm
tech.root: WinAuto
ms.assetid: 97AB327B-7A5D-C009-F430-42ADFC27F455
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IUIAutomationElement3, IUIAutomationElement3 interface [Windows Accessibility], IUIAutomationElement3 interface [Windows Accessibility],described, uiautomationclient/IUIAutomationElement3, winauto.uiauto_IUIAutomationElement3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationElement3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationElement3 interface


## -description


Extends the  <a href="https://msdn.microsoft.com/4D9A4E94-BAE9-4E85-8F21-7CABFBE64C6D">IUIAutomationElement2</a> interface. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationElement3</b> interface inherits from <a href="https://msdn.microsoft.com/97AB327B-7A5D-C009-F430-42ADFC27F455">IUIAutomationElement2</a>. <b>IUIAutomationElement3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationElement3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E41A7BE9-2383-EC27-7003-F0EB3CA62103">ShowContextMenu</a>
</td>
<td align="left" width="63%">
Programmatically invokes a context menu on the target element.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationElement3</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3F6D2EE1-CE3B-2E48-7539-555A44D1DBFD">CachedIsPeripheral</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached peripheral UI indicator for the element. Peripheral UI appears and supports user interaction, but does not take keyboard focus when it appears.  Examples of peripheral UI includes popups, flyouts, context menus, or floating notifications. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1E4B7D77-FCE7-9A1B-2D1A-A347A2F8C2B9">CurrentIsPeripheral</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the current peripheral UI indicator for the element.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/97AB327B-7A5D-C009-F430-42ADFC27F455">IUIAutomationElement2</a>



<a href="https://msdn.microsoft.com/dd7cdcf1-3511-424f-b729-b71a7e11cdd8">UI Automation Element Interfaces for Clients</a>
 

 

