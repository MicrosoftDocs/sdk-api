---
UID: NN:uiautomationclient.IUIAutomationProxyFactoryEntry
title: IUIAutomationProxyFactoryEntry
author: windows-sdk-content
description: Represents a proxy factory in the table maintained by Microsoft UI Automation, and exposes properties and methods that can be used by client applications to interact with IUIAutomationProxyFactory objects.
old-location: winauto\uiauto_IUIAutomationProxyFactoryEntry.htm
tech.root: WinAuto
ms.assetid: 0507deef-35dc-45bb-a7c1-82b84344ee17
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: IUIAutomationProxyFactoryEntry, IUIAutomationProxyFactoryEntry interface [Windows Accessibility], IUIAutomationProxyFactoryEntry interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationProxyFactoryEntry, uiauto_IUIAutomationProxyFactoryEntry, uiautomationclient/IUIAutomationProxyFactoryEntry, winauto.uiauto_IUIAutomationProxyFactoryEntry
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
 - IUIAutomationProxyFactoryEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationProxyFactoryEntry interface


## -description


Represents a proxy factory in the table maintained by Microsoft UI Automation, and exposes properties and methods that can be used by client applications to interact with <a href="https://msdn.microsoft.com/cdb2c94e-a5a7-41c3-b847-b23ea077abd3">IUIAutomationProxyFactory</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationProxyFactoryEntry</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationProxyFactoryEntry</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationProxyFactoryEntry</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8daa90f-9fad-48c7-8f22-e8c673fca330">GetWinEventsForAutomationEvent</a>
</td>
<td align="left" width="63%">
Retrieves the list of WinEvents that are mapped to a specific UI Automation event. If an element represented by this proxy raises one the listed WinEvents, the proxy handles it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/694cc14b-837c-4e09-b1e7-91bdc237657f">SetWinEventsForAutomationEvent</a>
</td>
<td align="left" width="63%">
Maps UI Automation events to WinEvents.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationProxyFactoryEntry</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8aa64070-7dd6-4a51-8458-6341daa856c7">AllowSubstringMatch</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that specifies whether the proxy allows substring matching.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c5a09754-4974-4742-ace8-55a2f290af83">CanCheckBaseClass</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that specifies whether the base class can be checked when searching for a proxy factory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d27bfdbb-dcdb-49d5-9871-9ac13b3b67f8">ClassName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the window class served by the proxy factory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7a3fde44-5b22-4686-9d48-4bc8b651cb37">ImageName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves the name of the image of the proxy factory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6a23b850-a2a0-4701-9725-e36213fcead7">NeedsAdviseEvents</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or retrieves a value that specifies whether the proxy must be notified when an application has registered for events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/da6f0c23-b16d-4fd5-8d91-cc5a830a03c6">ProxyFactory</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the proxy factory associated with this entry.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/46c6720a-19c2-4ddd-893c-1a46af0642fb">Proxy Factory Interfaces for Clients</a>
 

 

