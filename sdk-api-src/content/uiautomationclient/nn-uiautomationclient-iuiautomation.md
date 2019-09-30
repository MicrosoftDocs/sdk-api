---
UID: NN:uiautomationclient.IUIAutomation
title: IUIAutomation (uiautomationclient.h)
author: windows-sdk-content
description: Exposes methods that enable Microsoft UI Automation client applications to discover, access, and filter UI Automation elements.
old-location: winauto\uiauto_IUIAutomation.htm
tech.root: WinAuto
ms.assetid: 46b31ab6-39aa-4df8-a421-6369c32a9605
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomation, IUIAutomation interface [Windows Accessibility], IUIAutomation interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomation, uiauto_IUIAutomation, uiautomationclient/IUIAutomation, winauto.uiauto_IUIAutomation
ms.topic: interface
f1_keywords: 
 - "uiautomationclient/IUIAutomation"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation interface


## -description


Exposes methods that enable Microsoft UI Automation client applications to discover, access, and filter UI Automation elements. UI Automation exposes every element of the UI Automation as an object represented by the <b>IUIAutomation</b> interface. The members of this interface are not specific to a particular element.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomation</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addautomationeventhandler">AddAutomationEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles UI Automation events.

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler">AddFocusChangedEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles focus-changed events.

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler">AddPropertyChangedEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles and array of property-changed events. 

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray">AddPropertyChangedEventHandlerNativeArray</a>
</td>
<td align="left" width="63%">
Registers a method that handles a native array of property-changed events. 

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler">AddStructureChangedEventHandler</a>
</td>
<td align="left" width="63%">
Registers a method that handles structure-changed events.

<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-checknotsupported">CheckNotSupported</a>
</td>
<td align="left" width="63%">
Checks a provided <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> to see if it contains the Not Supported identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-compareelements">CompareElements</a>
</td>
<td align="left" width="63%">
Compares two UI Automation elements to determine whether they represent the same underlying UI element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-compareruntimeids">CompareRuntimeIds</a>
</td>
<td align="left" width="63%">
Compares two integer arrays containing run-time identifiers (IDs) to determine whether their content is the same and they belong to the same UI element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createandcondition">CreateAndCondition</a>
</td>
<td align="left" width="63%">
Creates a condition that selects elements that match both of two conditions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createandconditionfromarray">CreateAndConditionFromArray</a>
</td>
<td align="left" width="63%">
Creates a condition that selects elements based on multiple conditions, all of which must be true.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createandconditionfromnativearray">CreateAndConditionFromNativeArray</a>
</td>
<td align="left" width="63%">
Creates a condition that selects elements from a native array, based on multiple conditions that  must all be true.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createcacherequest">CreateCacheRequest</a>
</td>
<td align="left" width="63%">
Creates a cache request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createfalsecondition">CreateFalseCondition</a>
</td>
<td align="left" width="63%">
Creates a condition that is always false.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createnotcondition">CreateNotCondition</a>
</td>
<td align="left" width="63%">
Creates a condition that is the negative of a specified condition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createorcondition">CreateOrCondition</a>
</td>
<td align="left" width="63%">
Creates a combination of two conditions where a match exists if either of the conditions is true. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createorconditionfromarray">CreateOrConditionFromArray</a>
</td>
<td align="left" width="63%">
Creates a combination of two or more conditions where a match exists if any of the conditions is true. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createorconditionfromnativearray">CreateOrConditionFromNativeArray</a>
</td>
<td align="left" width="63%">
Creates a combination of two or more conditions where a match exists if any one of the conditions is true.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createpropertycondition">CreatePropertyCondition</a>
</td>
<td align="left" width="63%">
Creates a condition that selects elements that have a property with the specified value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createpropertyconditionex">CreatePropertyConditionEx</a>
</td>
<td align="left" width="63%">
Creates a condition that selects elements that have a property with the specified value, using optional flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry">CreateProxyFactoryEntry</a>
</td>
<td align="left" width="63%">
Creates a new instance of a proxy factory object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createtreewalker">CreateTreeWalker</a>
</td>
<td align="left" width="63%">
Retrieves a tree walker object that can be used to traverse the UI Automation tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-createtruecondition">CreateTrueCondition</a>
</td>
<td align="left" width="63%">
Retrieves a predefined condition that selects all elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-elementfromhandle">ElementFromHandle</a>
</td>
<td align="left" width="63%">
Retrieves a UI Automation element for the specified window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-elementfromhandlebuildcache">ElementFromHandleBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves a UI Automation element for the specified window, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-elementfromiaccessible">ElementFromIAccessible</a>
</td>
<td align="left" width="63%">
Retrieves a UI Automation element for the specified accessible object from a Microsoft Active Accessibility server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache">ElementFromIAccessibleBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves a UI Automation element for the specified accessible object from a Microsoft Active Accessibility server, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-elementfrompoint">ElementFromPoint</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element at the specified point on the desktop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-elementfrompointbuildcache">ElementFromPointBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element at the specified point on the desktop, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-getfocusedelement">GetFocusedElement</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element that has the input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-getfocusedelementbuildcache">GetFocusedElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element that has the input focus, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-getpatternprogrammaticname">GetPatternProgrammaticName</a>
</td>
<td align="left" width="63%">
Retrieves the registered programmatic name of a control pattern.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-getpropertyprogrammaticname">GetPropertyProgrammaticName</a>
</td>
<td align="left" width="63%">
Retrieves the registered programmatic name of a property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-getrootelement">GetRootElement</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element that represents the desktop.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-getrootelementbuildcache">GetRootElementBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation element that represents the desktop, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray">IntNativeArrayToSafeArray</a>
</td>
<td align="left" width="63%">
Converts an array of integers to a <a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray">IntSafeArrayToNativeArray</a>
</td>
<td align="left" width="63%">
Converts a <a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> of integers to an array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-pollforpotentialsupportedpatterns">PollForPotentialSupportedPatterns</a>
</td>
<td align="left" width="63%">
Retrieves the control patterns that might be supported on a UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-pollforpotentialsupportedproperties">PollForPotentialSupportedProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties that might be supported on a UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-recttovariant">RectToVariant</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://docs.microsoft.com/windows/desktop/WinAuto/variant-structure">VARIANT</a> that contains the coordinates of a rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removealleventhandlers">RemoveAllEventHandlers</a>
</td>
<td align="left" width="63%">
Removes all registered UI Automation event handlers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler">RemoveAutomationEventHandler</a>
</td>
<td align="left" width="63%">
Removes the specified UI Automation event handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler">RemoveFocusChangedEventHandler</a>
</td>
<td align="left" width="63%">
Removes a focus-changed event handler. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler">RemovePropertyChangedEventHandler</a>
</td>
<td align="left" width="63%">
Removes a property-changed event handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler">RemoveStructureChangedEventHandler</a>
</td>
<td align="left" width="63%">
Removes a structure-changed event handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray">SafeArrayToRectNativeArray</a>
</td>
<td align="left" width="63%">
Converts a <a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> containing rectangle coordinates to an array of type <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-varianttorect">VariantToRect</a>
</td>
<td align="left" width="63%">
Converts a <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> containing rectangle coordinates to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>.

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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_contentviewcondition">ContentViewCondition</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a predefined <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a> interface that selects content elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_contentviewwalker">ContentViewWalker</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtreewalker">IUIAutomationTreeWalker</a> interface used to discover content elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_controlviewcondition">ControlViewCondition</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a predefined <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a> interface that selects control elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_controlviewwalker">ControlViewWalker</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtreewalker">IUIAutomationTreeWalker</a> interface used to discover control elements.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping">ProxyFactoryMapping</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_rawviewcondition">RawViewCondition</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a predefined <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition">IUIAutomationCondition</a> interface that selects all UI elements in an unfiltered view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_rawviewwalker">RawViewWalker</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_reservedmixedattributevalue">ReservedMixedAttributeValue</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-get_reservednotsupportedvalue">ReservedNotSupportedValue</a>


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



Every UI Automation client application must obtain this interface to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)">CUIAutomation</a> object in order to gain access to the functionality of UI Automation.
	        

The following example function creates a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)">CUIAutomation</a> object and obtains the <b>IUIAutomation</b> interface.



```
IUIAutomation *g_pAutomation;

BOOL InitializeUIAutomation()
{
    CoInitialize(NULL);
    HRESULT hr = CoCreateInstance(__uuidof(CUIAutomation), NULL, CLSCTX_INPROC_SERVER, 
        __uuidof(IUIAutomation), (void**)&g_pAutomation);
    return (SUCCEEDED(hr));
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>
 

 

