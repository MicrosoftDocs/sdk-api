---
UID: NN:uiautomationclient.IUIAutomationLegacyIAccessiblePattern
title: IUIAutomationLegacyIAccessiblePattern
author: windows-sdk-content
description: Exposes methods and properties that enable Microsoft UI Automation clients to retrieve UI information from Microsoft Active Accessibility (MSAA) servers.
old-location: winauto\uiauto_IUIAutomationLegacyIAccessiblePattern.htm
tech.root: WinAuto
ms.assetid: d6564d14-a739-47bf-9202-0757ac3ba7f8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIAutomationLegacyIAccessiblePattern, IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility], IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern, uiauto_IUIAutomationLegacyIAccessiblePattern, uiautomationclient/IUIAutomationLegacyIAccessiblePattern, winauto.uiauto_IUIAutomationLegacyIAccessiblePattern
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IUIAutomationLegacyIAccessiblePattern
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationLegacyIAccessiblePattern interface


## -description


Exposes methods and properties that enable Microsoft UI Automation clients to retrieve UI information from Microsoft Active Accessibility (MSAA) servers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationLegacyIAccessiblePattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationLegacyIAccessiblePattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationLegacyIAccessiblePattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b518a835-02f5-48ce-a70b-792abf8b4306">DoDefaultAction</a>
</td>
<td align="left" width="63%">
Performs the Microsoft Active Accessibility default action for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/923c3f64-7205-4d41-b726-90324e65661e">GetCachedSelection</a>
</td>
<td align="left" width="63%">
Retrieves the cached Microsoft Active Accessibility property that identifies the selected children of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fe666dc-2168-44a0-87f2-f444fd2a70f2">GetCurrentSelection</a>
</td>
<td align="left" width="63%">
Retrieves the Microsoft Active Accessibility property that identifies the selected children of this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58ce3005-dfac-4ffe-b874-69a2f994e7a6">GetIAccessible</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> object that corresponds to the UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d311a10d-4762-47c9-a0bd-299da43827f7">Select</a>
</td>
<td align="left" width="63%">
Performs a Microsoft Active Accessibility selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5891bb3-e727-430c-a4d4-5c59750b01ce">SetValue</a>
</td>
<td align="left" width="63%">
Sets the Microsoft Active Accessibility value property for the element.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationLegacyIAccessiblePattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/31b64e45-51dc-485a-8318-2e8db690f3c0">CachedChildId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached Microsoft Active Accessibility child identifier for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/acd43075-4f53-48d3-a039-0882a4833d9e">CachedDefaultAction</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the Microsoft Active Accessibility default action for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/707cf9d2-5c29-4eb2-aba2-5c5199e7292c">CachedDescription</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached Microsoft Active Accessibility description of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/66ce70ed-e76e-4a31-8dae-0ab4abd6c982">CachedHelp</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached Microsoft Active Accessibility help string for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3ebe588d-19ab-4df2-be01-4abd0a62a2f8">CachedKeyboardShortcut</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached Microsoft Active Accessibility keyboard shortcut property for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/eda01409-fdb7-4dc8-844a-699120db8771">CachedName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached Microsoft Active Accessibility name property of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/efa5ff74-1322-49ab-a7b9-f4394b3c6e64">CachedRole</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached Microsoft Active Accessibility role of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0429138e-e218-4384-be21-666fe5ca5542">CachedState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached Microsoft Active Accessibility state identifier for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/864c99b5-a5ab-486d-ac0d-1471698a8de4">CachedValue</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached Microsoft Active Accessibility value property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/63277b76-bd3f-4255-82be-24797cafd175">CurrentChildId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the Microsoft Active Accessibility child identifier for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d9fe2161-db5a-4e41-9f07-17cb3e4ce78a">CurrentDefaultAction</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the Microsoft Active Accessibility default action for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bdadeb0f-4739-4d0c-bd41-17ac9addf933">CurrentDescription</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the Microsoft Active Accessibility description of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fb4d8ca3-2263-46f6-875f-78973bd355d5">CurrentHelp</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the Microsoft Active Accessibility help string for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c0b205d3-b36a-4ad5-9d4a-f9d8a1ab7701">CurrentKeyboardShortcut</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the Microsoft Active Accessibility keyboard shortcut property for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8e1138dc-212d-409e-8c69-8f94320c3dd6">CurrentName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the Microsoft Active Accessibility name property of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9159e114-edc6-4dfa-b32f-a5a786dabe99">CurrentRole</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the Microsoft Active Accessibility role identifier of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/255e8900-e25a-43e4-b943-60a1814d342d">CurrentState</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the Microsoft Active Accessibility state identifier for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/48f960f1-113a-4ab8-809d-e83a7a66c28c">CurrentValue</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the Microsoft Active Accessibility value property.

</td>
</tr>
</table> 


## -remarks



This interface is obtained just like any other control pattern. It enables UI Automation clients to gather MSAA properties more efficiently, taking advantage of the caching system, and also enables UI Automation clients to interact with native Microsoft Active Accessibility servers that support the <b>IAccessible</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

