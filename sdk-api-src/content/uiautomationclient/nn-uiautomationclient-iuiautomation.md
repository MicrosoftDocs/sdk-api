---
UID: NN:uiautomationclient.IUIAutomation
title: IUIAutomation
author: windows-sdk-content
description: Exposes methods that enable Microsoft UI Automation client applications to discover, access, and filter UI Automation elements.
old-location: winauto\uiauto_IUIAutomation.htm
tech.root: WinAuto
ms.assetid: 46b31ab6-39aa-4df8-a421-6369c32a9605
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IUIAutomation, IUIAutomation interface [Windows Accessibility], IUIAutomation interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomation, uiauto_IUIAutomation, uiautomationclient/IUIAutomation, winauto.uiauto_IUIAutomation
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
 - IUIAutomation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation interface


## -description


Exposes methods that enable Microsoft UI Automation client applications to discover, access, and filter UI Automation elements. UI Automation exposes every element of the UI Automation as an object represented by the <b>IUIAutomation</b> interface. The members of this interface are not specific to a particular element.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15ceca71-33e8-4d66-afd6-3d50fe81c127">AddAutomationEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles UI Automation events.

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/469e9c3e-366f-4c13-8c27-58fdb705d4d9">AddFocusChangedEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles focus-changed events.

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2623a48e-8818-486c-9bde-b218cde49189">AddPropertyChangedEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles property-changed events. 

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d3cf5c3-5d0e-4214-a9fc-8b0132ad9b77">AddPropertyChangedEventHandlerNativeArray</a>
</td>
<td align="left" width="63%">
Registers a method that handles property-changed events. 

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/671049a4-50cf-49df-9028-7af38629b7a9">AddStructureChangedEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles structure-changed events.

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7fd7d1e-3f7b-4700-9263-2cab6e0de896">CheckNotSupported</a>
</td>
<td align="left" width="63%">
Checks a provided <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-tagvariant">VARIANT</a> to see if it contains the Not Supported identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4daa3c3-24fb-41df-a1b1-bd6545a47e51">CompareElements</a>
</td>
<td align="left" width="63%">
Compares two UI Automation elements to determine whether they represent the same underlying UI element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0c481eb-3545-439c-bf6a-347b98ea35de">CompareRuntimeIds</a>
</td>
<td align="left" width="63%">
Compares two integer arrays containing run-time identifiers (IDs) to determine whether their content is the same and they belong to the same UI element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/066476b4-586c-477c-82ee-de2f2074d63b">CreateAndCondition</a>
</td>
<td align="left" width="63%">
Creates a condition that selects elements that match both of two conditions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec9ad1a1-72c7-4fc6-8812-577b44b4c5eb">CreateAndConditionFromArray</a>
</td>
<td align="left" width="63%">
Creates a condition that selects elements based on multiple conditions, all of which must be true.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f47dfa7-1558-4984-8400-cac549543819">CreateAndConditionFromNativeArray</a>
</td>
<td align="left" width="63%">
Creates a condition that selects elements based on multiple conditions, all of which must be true.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e61aecac-8c08-4f83-b3e6-f4baedcb16c6">CreateCacheRequest</a>
</td>
<td align="left" width="63%">
Creates a cache request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fee46b7-a186-48b8-8fc0-f9844a2b6d8d">CreateFalseCondition</a>
</td>
<td align="left" width="63%">
Creates a condition that is always false.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/183603f9-6e5b-4c44-b6b2-c363b4d150c3">CreateNotCondition</a>
</td>
<td align="left" width="63%">
Creates a condition that is the negative of a specified condition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17e83b94-21f0-44b6-87be-3fc44b0dc5a0">CreateOrCondition</a>
</td>
<td align="left" width="63%">
Creates a combination of two conditions where a match exists if either of the conditions is true. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/acd15fd0-ac15-4477-8e89-4d7a4f9c93c6">CreateOrConditionFromArray</a>
</td>
<td align="left" width="63%">
Creates a combination of two or more conditions where a match exists if any of the conditions is true. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/393c777c-f262-462b-ac59-035f590bee1c">CreateOrConditionFromNativeArray</a>
</td>
<td align="left" width="63%">
Creates a combination of two or more conditions where a match exists if any one of the conditions is true.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b777a53-90a8-4e51-b707-d0ea8f5790a8">CreatePropertyCondition</a>
</td>
<td align="left" width="63%">
Creates a condition that selects elements that have a property with the specified value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc7ad9e8-b315-40b1-af02-997a38c4ee66">CreatePropertyConditionEx</a>
</td>
<td align="left" width="63%">
Creates a condition that selects elements that have a property with the specified value, using optional flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dcb7ceb8-d794-4b7a-97ed-d7fc2002d7d7">CreateProxyFactoryEntry</a>
</td>
<td align="left" width="63%">
Creates a new instance of a proxy factory object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c976bf97-656b-4992-b0c5-f442b501ad75">CreateTreeWalker</a>
</td>
<td align="left" width="63%">
Retrieves a tree walker object that can be used to traverse the UI Automation tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02f55293-5d2d-4578-9c31-3ed04dac428e">CreateTrueCondition</a>
</td>
<td align="left" width="63%">
Retrieves a predefined condition that selects all elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07c6b7fa-80af-44c2-abcf-a167385892d5">ElementFromHandle</a>
</td>
<td align="left" width="63%">
Retrieves a UI Automation element for the specified window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6c1e03b-7c0e-4dee-b276-bfc7d6247d4e">ElementFromHandleBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves a UI Automation element for the specified window, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3dcc31c-e111-4841-82a8-a6329020b595">ElementFromIAccessible</a>
</td>
<td align="left" width="63%">
Retrieves a UI Automation element for the specified accessible object from a Microsoft Active Accessibility server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7feadfc9-0be3-40ec-a986-526b207d1f38">ElementFromIAccessibleBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves a UI Automation element for the specified accessible object from a Microsoft Active Accessibility server, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4233cc97-94c8-4861-a364-823cca1e5ff8">ElementFromPoint</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element at the specified point on the desktop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb3a8773-270a-4e33-bcbe-bde7794ea4ad">ElementFromPointBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element at the specified point on the desktop, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a75f03bc-f472-40bf-8fa2-8c1d3ddf4fbb">GetFocusedElement</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element that has the input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c37c2703-ce01-44fe-a959-33b9f7d66e98">GetFocusedElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element that has the input focus, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5968193-e3d9-41d1-b13f-8e86db5e0c70">GetPatternProgrammaticName</a>
</td>
<td align="left" width="63%">
Retrieves the registered programmatic name of a control pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4472de0-7194-411d-a508-a5d81aba8b7d">GetPropertyProgrammaticName</a>
</td>
<td align="left" width="63%">
Retrieves the registered programmatic name of a property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b6f3a78-a957-4ebd-a026-a8edb30faa88">GetRootElement</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element that represents the desktop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d2c0592-d29a-4e70-978e-55690aed82cb">GetRootElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element that represents the desktop, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8fd2c2b-f8c7-454b-ad03-aeeb4bbcef61">IntNativeArrayToSafeArray</a>
</td>
<td align="left" width="63%">
Converts an array of integers to a <a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/422b1bfc-5f67-4ba5-b573-d3dce9b6d806">IntSafeArrayToNativeArray</a>
</td>
<td align="left" width="63%">
Converts a <a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> of integers to an array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1319420e-17d6-4d0f-81c5-46b22b644e68">PollForPotentialSupportedPatterns</a>
</td>
<td align="left" width="63%">
Retrieves the control patterns that might be supported on a UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2cb78604-3c61-4362-9d8a-e40d5ddb4047">PollForPotentialSupportedProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties that might be supported on a UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abfb2bb1-7594-4f32-9188-05745006ae18">RectToVariant</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a> that contains the coordinates of a rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bf6d15a-2aaf-4f94-a852-f9cbd25cd496">RemoveAllEventHandlers</a>
</td>
<td align="left" width="63%">
Removes all registered UI Automation event handlers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4ebf7d3-c3c4-424b-af69-b8c13dd7a4dd">RemoveAutomationEventHandler</a>
</td>
<td align="left" width="63%">
Removes the specified UI Automation event handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96913631-76e0-405a-888d-ac7f6485a18e">RemoveFocusChangedEventHandler</a>
</td>
<td align="left" width="63%">
Removes a focus-changed event handler. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8f7600f-a33e-4f30-ae8e-423f9c71edbe">RemovePropertyChangedEventHandler</a>
</td>
<td align="left" width="63%">
Removes a property-changed event handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0f8bb2a-003f-471f-b1a6-ffec97e2752a">RemoveStructureChangedEventHandler</a>
</td>
<td align="left" width="63%">
Removes a structure-changed event handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fa9fad1-55b9-4cb5-a5c2-687074fa5d56">SafeArrayToRectNativeArray</a>
</td>
<td align="left" width="63%">
Converts a <a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> containing rectangle coordinates to an array of type <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef8bb8eb-c6f1-4797-b64f-f4f9d41db2bb">VariantToRect</a>
</td>
<td align="left" width="63%">
Converts a <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-tagvariant">VARIANT</a> containing rectangle coordinates to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomation</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d674a8c5-cb09-49a6-b457-5e7486b0e178">ContentViewCondition</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a predefined <a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a> interface that selects content elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f34b7631-1d95-4c2e-b3fc-7600d5b24b15">ContentViewWalker</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/adb4afed-63b9-42b4-8a8d-673d4813bb52">IUIAutomationTreeWalker</a> interface used to discover content elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1dbe6ce9-6fa4-42c6-bece-e9ae20ef9837">ControlViewCondition</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a predefined <a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a> interface that selects control elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e2b22ed2-9f86-405d-98ce-0f789a3159dc">ControlViewWalker</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/adb4afed-63b9-42b4-8a8d-673d4813bb52">IUIAutomationTreeWalker</a> interface used to discover control elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cf1aae6e-3f83-4b4e-9e5c-a57db6cfa9ce">ProxyFactoryMapping</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an object that represents the mapping of Window classnames and associated data to individual proxy factories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2ed9867c-2bcb-464e-a5a6-15e9f4dcd276">RawViewCondition</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a predefined <a href="https://msdn.microsoft.com/66515d42-2b98-4923-b326-9fec557345b7">IUIAutomationCondition</a> interface that selects all UI elements in an unfiltered view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1c76140d-50da-41d6-a997-926396f37a36">RawViewWalker</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a tree walker object used to traverse an unfiltered view of the UI Automation tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5b225507-deee-4f2c-a17b-f0e96963a1d0">ReservedMixedAttributeValue</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a static token object representing a text attribute that is a mixed attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/00162b3c-fab8-4559-83c0-d8c6731441c3">ReservedNotSupportedValue</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a static token object representing a property or text attribute that is not supported.

</td>
</tr>
</table> 


## -remarks



Every UI Automation client application must obtain this interface to a <a href="https://msdn.microsoft.com/5a3a108d-48da-4384-9f38-052b9ff6d7aa">CUIAutomation</a> object in order to gain access to the functionality of UI Automation.
	        

The following example function creates a <a href="https://msdn.microsoft.com/5a3a108d-48da-4384-9f38-052b9ff6d7aa">CUIAutomation</a> object and obtains the <b>IUIAutomation</b> interface.


<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IUIAutomation *g_pAutomation;

BOOL InitializeUIAutomation()
{
    CoInitialize(NULL);
    HRESULT hr = CoCreateInstance(__uuidof(CUIAutomation), NULL, CLSCTX_INPROC_SERVER, 
        __uuidof(IUIAutomation), (void**)&amp;g_pAutomation);
    return (SUCCEEDED(hr));
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dd7cdcf1-3511-424f-b729-b71a7e11cdd8">UI Automation Element Interfaces for Clients</a>
 

 

