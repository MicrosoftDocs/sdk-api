---
UID: NN:uiautomationclient.IUIAutomationElement
title: IUIAutomationElement
author: windows-sdk-content
description: Exposes methods and properties for a UI Automation element, which represents a UI item.
old-location: winauto\uiauto_IUIAutomationElement.htm
old-project: WinAuto
ms.assetid: 9e1f87b1-a204-4ca9-acf2-a40277012207
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: IUIAutomationElement, IUIAutomationElement interface [Windows Accessibility], IUIAutomationElement interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationElement, uiauto_IUIAutomationElement, uiautomationclient/IUIAutomationElement, winauto.uiauto_IUIAutomationElement
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
 - IUIAutomationElement
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationElement interface


## -description


Exposes methods and properties for a UI Automation element, which represents a UI item. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationElement</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationElement</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationElement</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2499b3c-433f-4e2f-937c-78da66c16203">BuildUpdatedCache</a>
</td>
<td align="left" width="63%">
Retrieves a new UI Automation element with an updated cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ead73c6d-7fb8-4e00-b027-5d747268af08">FindAll</a>
</td>
<td align="left" width="63%">
Returns all UI Automation elements that satisfy the specified condition. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/acf16f88-2b68-4fd4-b715-b3a61340bdd0">FindAllBuildCache</a>
</td>
<td align="left" width="63%">
Returns all UI Automation elements that satisfy the specified condition, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84098431-46e8-49bd-a258-337ad1d68f91">FindFirst</a>
</td>
<td align="left" width="63%">
Retrieves the first child or descendant element that matches the specified condition. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecb10fbf-ff1d-4bd0-b036-1050560d82fe">FindFirstBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the first child or descendant element that matches the specified condition, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dab24be3-0e0e-445f-a9cc-bb2733916cdc">GetCachedChildren</a>
</td>
<td align="left" width="63%">
Retrieves the cached child elements of this UI Automation element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10ca955b-416a-47c0-9970-940d98132b38">GetCachedParent</a>
</td>
<td align="left" width="63%">
Retrieves from the cache the parent of this UI Automation element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c71cab11-24c7-4e66-bcf2-f1abb1f37abb">GetCachedPattern</a>
</td>
<td align="left" width="63%">
Retrieves from the cache the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the specified control pattern of this UI Automation element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d0170e2-277e-48f8-a2e4-5c4ece92d8ec">GetCachedPatternAs</a>
</td>
<td align="left" width="63%">
Retrieves the control pattern interface of the specified pattern from the cache of this UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cd093fe-04ee-4b09-b5e7-28dad984951e">GetCachedPropertyValue</a>
</td>
<td align="left" width="63%">
Retrieves a property value from the cache for this UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f496ee4-8508-4331-9c1c-7805e17874f9">GetCachedPropertyValueEx</a>
</td>
<td align="left" width="63%">
Retrieves a property value from the cache for this UI Automation element, optionally ignoring any default value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3762aac6-5bd8-43a6-8fe6-e79d8724622b">GetClickablePoint</a>
</td>
<td align="left" width="63%">
Retrieves a point on the element that can be clicked. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ad4df7c-979d-464f-9600-d1f3de064b59">GetCurrentPattern</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the specified control pattern on this UI Automation element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98b0f647-7f6e-4e07-8530-1dae781507bc">GetCurrentPatternAs</a>
</td>
<td align="left" width="63%">
Retrieves the control pattern interface of the specified pattern on this UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/819e548e-7ff4-4f9f-969b-bfd1625f6151">GetCurrentPropertyValue</a>
</td>
<td align="left" width="63%">
Retrieves the current value of a property for this UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3adbd380-4500-4701-bfc3-dc03d51e5155">GetCurrentPropertyValueEx</a>
</td>
<td align="left" width="63%">
Retrieves a property value for this UI Automation element, optionally ignoring any default value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d351f2ca-d9de-4055-8356-9a100a77f397">GetRuntimeId</a>
</td>
<td align="left" width="63%">
Retrieves the unique identifier assigned to the UI element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a4e549a-1812-4380-bc0a-2da579a62b5d">SetFocus</a>
</td>
<td align="left" width="63%">
Sets the keyboard focus to this UI Automation element.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationElement</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/52767d3d-7cda-4973-894b-d5e5996c7439">CachedAcceleratorKey</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached accelerator key for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dc4394b3-f609-4709-b9b5-c8bf84d17b3f">CachedAccessKey</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached access key character for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0156348c-4c3a-4351-9bcc-16e8f4107916">CachedAriaProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached ARIA properties of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8e3671b0-49f5-4d8b-b2ab-51a976316191">CachedAriaRole</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached ARIA role of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1449dfe7-c0b9-4920-af7a-34aa4f036156">CachedAutomationId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached UI Automation identifier of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/31e171e1-b688-45ab-8bc3-971d9f61db3c">CachedBoundingRectangle</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached coordinates of the rectangle that completely encloses the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7b5e9c75-5190-4cdd-9774-0c883747018c">CachedClassName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached class name of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/09d9157c-e9e0-4647-9637-d95b66937245">CachedControllerFor</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached array of UI Automation elements for which this element serves as the controller.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/48b232a8-8826-4c70-b541-3e6a792105c1">CachedControlType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates the control type of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9961ee21-d9b7-4ff6-a8ee-ad45ba1cd142">CachedCulture</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates the culture associated with the element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/705c9f5a-ef7d-4495-8de2-710a6e9f78df">CachedDescribedBy</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached array of elements  that describe this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/22ef02fb-ee75-4067-a99b-a940a311347c">CachedFlowsTo</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached array of elements that indicate the reading order after the current element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/da793d93-276b-47ea-a78f-bbdd83f1bc07">CachedFrameworkId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached name of the underlying UI framework associated with the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/89c69ac7-4b2e-44a4-a516-0403448c61b4">CachedHasKeyboardFocus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
A cached value that indicates whether the element has keyboard focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/39ca5d50-808c-4a8b-a662-0a7724519b2c">CachedHelpText</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached help text for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3e06c0dd-0cdd-4193-9353-5a71d08ec17d">CachedIsContentElement</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
A cached value that indicates whether the element is a content element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3d8b1b5e-4e68-454a-9cfc-dd742a5fa760">CachedIsControlElement</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the element is a control element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2f1027fd-7d95-412f-a9e8-73236252e49f">CachedIsDataValidForForm</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the element contains valid data for the form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e3b6bf79-51a7-46bf-91af-4448df8e4be7">CachedIsEnabled</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the element is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ccb10e4f-9d44-452a-99dd-f29290fe720d">CachedIsKeyboardFocusable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the element can accept keyboard focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2c063a7a-8422-4ebd-b58b-944f93ba9e69">CachedIsOffscreen</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the element is off-screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2e73bc18-851f-4675-9439-5687c5133a3d">CachedIsPassword</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the element contains a disguised password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d1edcdfb-0020-4d38-a1e7-4b2d9555bd21">CachedIsRequiredForForm</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether the element is required to be filled out on a form. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/29a7e815-9d86-49e3-81b0-bf9398f27cad">CachedItemStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached description of the status of an item within an element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/66b9180c-ebde-4e5a-b431-f81a094a0ee4">CachedItemType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached string that describes the type of item represented by the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a0c76cf1-1c59-40b9-8bb7-9a2e68bef4a9">CachedLabeledBy</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached element that contains the text label for this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/815cce32-45ca-4fd1-aedc-5b288d876d60">CachedLocalizedControlType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached localized description of the control type of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9d70a40c-9bcf-4ca9-90dd-05d25ddb7e89">CachedName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached name of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d7f14d89-20a2-4cfe-9a1b-31df442a5b77">CachedNativeWindowHandle</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached window handle of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2ae8be5f-fa10-4350-b80e-89bb32baf56c">CachedOrientation</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates the orientation of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/16a3470d-cbea-4cc2-96d5-668c748abab2">CachedProcessId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached ID of the process that hosts the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ed26dbb7-9838-48f2-8401-f169038b8b92">CachedProviderDescription</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached description of the provider for this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/393f63b4-e3f4-4b62-af92-1fb9bee079ba">CurrentAcceleratorKey</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the accelerator key for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0da10db5-a978-4575-86c4-12152691468f">CurrentAccessKey</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the access key character for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/40c5ec95-9317-4123-8f9f-fe34b6c983b7">CurrentAriaProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the ARIA properties of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/469c0d3d-3063-4000-b18c-82b2c81482fa">CurrentAriaRole</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the ARIA role of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d8dbf803-44ad-4ec6-a1b3-098c85da2364">CurrentAutomationId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the UI Automation identifier of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bf3e96ca-1fda-417a-9614-6a1a3923ce7e">CurrentBoundingRectangle</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the coordinates of the rectangle that completely encloses the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/df019800-7467-48ef-8c16-0cb8c8d05ed5">CurrentClassName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the class name of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/48a0b904-2682-4b1e-ad07-3d2ef6a24f14">CurrentControllerFor</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an array of elements for which this element serves as the controller.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6bceeabd-be77-4820-842a-d343fa2857bd">CurrentControlType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the control type of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/369edad8-6629-41a9-82cb-386a6c02f5f9">CurrentCulture</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the culture identifier for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/059d623e-d312-4427-bb2d-a1431dc68ccd">CurrentDescribedBy</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an array of elements that describe this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4b807101-1a80-4f2b-a1d3-a08cd654ec44">CurrentFlowsTo</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an array of elements that indicates the reading order after the current element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b54af8d4-87b1-4fd3-bc25-1a7c038899ea">CurrentFrameworkId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of the underlying UI framework.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/90ef17df-1658-4199-8e8c-0cd21724dcf6">CurrentHasKeyboardFocus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the element has keyboard focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/02ecfecc-5c3d-458b-827a-a598b8f98916">CurrentHelpText</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the help text for the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9fc8aada-cb6e-497e-b915-a22117788012">CurrentIsContentElement</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the element is a content element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9205db9b-becd-4485-8cba-516b6842b44f">CurrentIsControlElement</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the element is a control element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/002d87c4-5389-4dc4-8253-484b8d2f28f9">CurrentIsDataValidForForm</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the element contains valid data for a form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/65b1311d-479a-4be4-a9fb-7dfe885420b8">CurrentIsEnabled</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the element is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/44c4d5a6-2f31-4707-bcd5-bb1c06d2e3ce">CurrentIsKeyboardFocusable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the element can accept keyboard focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/51bec7bd-a547-4c75-ab8a-ebdd9bbd6c01">CurrentIsOffscreen</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the element is off-screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d2af875b-a0d6-41e1-8eec-a38f42fff7ac">CurrentIsPassword</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the element contains a disguised password.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/30482395-1d26-4f86-868c-4c46d5375c00">CurrentIsRequiredForForm</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the element is required to be filled out on a form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a0bac87a-96ad-4b5a-9179-3149580cb18c">CurrentItemStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the description of the status of an item in an element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/773960d8-40f2-4015-9b9d-6bfc05a72115">CurrentItemType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a description of the type of UI item represented by the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e461cc68-5a67-424b-9fc6-0768b9e13346">CurrentLabeledBy</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the element that contains the text label for this element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/72e60876-ecda-411a-8d90-a96827c66453">CurrentLocalizedControlType</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a localized description of the control type of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1a56f9ae-ac5a-4444-8ab4-083db124ead6">CurrentName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9a59f674-6b48-4679-bc24-fe46ebae2041">CurrentNativeWindowHandle</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the window handle of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9afe358e-b80c-40f8-be0a-1f07346bb583">CurrentOrientation</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that indicates the orientation of the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c230cd82-99f9-4922-9626-cb67fa2942c1">CurrentProcessId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the identifier of the process that hosts the element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d6a303b4-5540-45d3-b3c2-9b98b58a90bb">CurrentProviderDescription</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a description of the provider for this element.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dd7cdcf1-3511-424f-b729-b71a7e11cdd8">UI Automation Element Interfaces for Clients</a>
 

 

