---
UID: NN:uiautomationclient.IUIAutomationProxyFactoryMapping
title: IUIAutomationProxyFactoryMapping
author: windows-sdk-content
description: Exposes properties and methods for a table of proxy factories. Each table entry is represented by an IUIAutomationProxyFactoryEntry interface. The entries are in the order in which the system will attempt to use the proxies.
old-location: winauto\uiauto_IUIAutomationProxyFactoryMapping.htm
old-project: WinAuto
ms.assetid: 7a938c1c-a11c-4fdd-a73a-e7656032f21e
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IUIAutomationProxyFactoryMapping, IUIAutomationProxyFactoryMapping interface [Windows Accessibility], IUIAutomationProxyFactoryMapping interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationProxyFactoryMapping, uiauto_IUIAutomationProxyFactoryMapping, uiautomationclient/IUIAutomationProxyFactoryMapping, winauto.uiauto_IUIAutomationProxyFactoryMapping
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
 - IUIAutomationProxyFactoryMapping
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationProxyFactoryMapping interface


## -description


Exposes properties and methods for a table of proxy factories. Each table entry is represented by an <a href="https://msdn.microsoft.com/0507deef-35dc-45bb-a7c1-82b84344ee17">IUIAutomationProxyFactoryEntry</a> interface. The entries are in the order in which the system will attempt to use the proxies.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationProxyFactoryMapping</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationProxyFactoryMapping</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationProxyFactoryMapping</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00f16e39-557c-4e55-bfbf-49dc0d97ab37">ClearTable</a>
</td>
<td align="left" width="63%">
Removes all entries from the proxy factory table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1500c5e5-5161-4753-ab3a-7e5b62246411">GetEntry</a>
</td>
<td align="left" width="63%">
Retrieves an entry from the proxy factory table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e84ec4d-9589-47b0-ae69-5d640141dd8b">GetTable</a>
</td>
<td align="left" width="63%">
Retrieves all entries in the proxy factory table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f398a1b5-d558-4187-9ee5-147b139d99e0">InsertEntries</a>
</td>
<td align="left" width="63%">
Inserts entries into the table of proxy factories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe737909-0331-4c5f-8d38-8dce09bd2e44">InsertEntry</a>
</td>
<td align="left" width="63%">
Insert an entry into the table of proxy factories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a09fbda-9e95-4f31-b669-e68310071aa9">RemoveEntry</a>
</td>
<td align="left" width="63%">
Removes an entry from the table of proxy factories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adf9ca6d-4206-4b7e-b43c-0701fdeb1b23">RestoreDefaultTable</a>
</td>
<td align="left" width="63%">
Restores the default table of proxy factories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b3675a4-a4d5-40ed-bb11-7e4d50746019">SetTable</a>
</td>
<td align="left" width="63%">
Sets the table of proxy factories.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationProxyFactoryMapping</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of entries in the proxy factory table.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/46c6720a-19c2-4ddd-893c-1a46af0642fb">Proxy Factory Interfaces for Clients</a>
 

 

