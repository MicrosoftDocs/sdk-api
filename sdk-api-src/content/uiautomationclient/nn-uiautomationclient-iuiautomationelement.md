---
UID: NN:uiautomationclient.IUIAutomationElement
title: IUIAutomationElement (uiautomationclient.h)
description: Exposes methods and properties for a UI Automation element, which represents a UI item.
helpviewer_keywords: ["IUIAutomationElement","IUIAutomationElement interface [Windows Accessibility]","IUIAutomationElement interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationElement","uiauto_IUIAutomationElement","uiautomationclient/IUIAutomationElement","winauto.uiauto_IUIAutomationElement"]
old-location: winauto\uiauto_IUIAutomationElement.htm
tech.root: WinAuto
ms.assetid: 9e1f87b1-a204-4ca9-acf2-a40277012207
ms.date: 12/05/2018
ms.keywords: IUIAutomationElement, IUIAutomationElement interface [Windows Accessibility], IUIAutomationElement interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationElement, uiauto_IUIAutomationElement, uiautomationclient/IUIAutomationElement, winauto.uiauto_IUIAutomationElement
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationElement
 - uiautomationclient/IUIAutomationElement
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomationElement
---

# IUIAutomationElement interface


## -description

Exposes methods and properties for a UI Automation element, which represents a UI item.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationElement</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationElement</b> also has these types of members:
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
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache">BuildUpdatedCache</a>
</td>
<td align="left" width="63%">
Retrieves a new UI Automation element with an updated cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findall">FindAll</a>
</td>
<td align="left" width="63%">
Returns all UI Automation elements that satisfy the specified condition. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findallbuildcache">FindAllBuildCache</a>
</td>
<td align="left" width="63%">
Returns all UI Automation elements that satisfy the specified condition, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirst">FindFirst</a>
</td>
<td align="left" width="63%">
Retrieves the first child or descendant element that matches the specified condition. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache">FindFirstBuildCache</a>
</td>
<td align="left" width="63%">
Retrieves the first child or descendant element that matches the specified condition, prefetches the requested properties and control patterns, and stores the prefetched items in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedchildren">GetCachedChildren</a>
</td>
<td align="left" width="63%">
Retrieves the cached child elements of this UI Automation element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedparent">GetCachedParent</a>
</td>
<td align="left" width="63%">
Retrieves from the cache the parent of this UI Automation element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedpattern">GetCachedPattern</a>
</td>
<td align="left" width="63%">
Retrieves from the cache the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the specified control pattern of this UI Automation element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas">GetCachedPatternAs</a>
</td>
<td align="left" width="63%">
Retrieves the control pattern interface of the specified pattern from the cache of this UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue">GetCachedPropertyValue</a>
</td>
<td align="left" width="63%">
Retrieves a property value from the cache for this UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex">GetCachedPropertyValueEx</a>
</td>
<td align="left" width="63%">
Retrieves a property value from the cache for this UI Automation element, optionally ignoring any default value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getclickablepoint">GetClickablePoint</a>
</td>
<td align="left" width="63%">
Retrieves a point on the element that can be clicked. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern">GetCurrentPattern</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the specified control pattern on this UI Automation element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas">GetCurrentPatternAs</a>
</td>
<td align="left" width="63%">
Retrieves the control pattern interface of the specified pattern on this UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue">GetCurrentPropertyValue</a>
</td>
<td align="left" width="63%">
Retrieves the current value of a property for this UI Automation element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex">GetCurrentPropertyValueEx</a>
</td>
<td align="left" width="63%">
Retrieves a property value for this UI Automation element, optionally ignoring any default value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getruntimeid">GetRuntimeId</a>
</td>
<td align="left" width="63%">
Retrieves the unique identifier assigned to the UI element. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-setfocus">SetFocus</a>
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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedacceleratorkey">CachedAcceleratorKey</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedaccesskey">CachedAccessKey</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedariaproperties">CachedAriaProperties</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedariarole">CachedAriaRole</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedautomationid">CachedAutomationId</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle">CachedBoundingRectangle</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedclassname">CachedClassName</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedcontrollerfor">CachedControllerFor</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype">CachedControlType</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedculture">CachedCulture</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cacheddescribedby">CachedDescribedBy</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedflowsto">CachedFlowsTo</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedframeworkid">CachedFrameworkId</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedhaskeyboardfocus">CachedHasKeyboardFocus</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext">CachedHelpText</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachediscontentelement">CachedIsContentElement</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachediscontrolelement">CachedIsControlElement</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedisdatavalidforform">CachedIsDataValidForForm</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedisenabled">CachedIsEnabled</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachediskeyboardfocusable">CachedIsKeyboardFocusable</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedisoffscreen">CachedIsOffscreen</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedispassword">CachedIsPassword</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedisrequiredforform">CachedIsRequiredForForm</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cacheditemstatus">CachedItemStatus</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cacheditemtype">CachedItemType</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedlabeledby">CachedLabeledBy</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedlocalizedcontroltype">CachedLocalizedControlType</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedname">CachedName</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachednativewindowhandle">CachedNativeWindowHandle</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedorientation">CachedOrientation</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedprocessid">CachedProcessId</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedproviderdescription">CachedProviderDescription</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentacceleratorkey">CurrentAcceleratorKey</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentaccesskey">CurrentAccessKey</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentariaproperties">CurrentAriaProperties</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentariarole">CurrentAriaRole</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentautomationid">CurrentAutomationId</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle">CurrentBoundingRectangle</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentclassname">CurrentClassName</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentcontrollerfor">CurrentControllerFor</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype">CurrentControlType</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentculture">CurrentCulture</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentdescribedby">CurrentDescribedBy</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentflowsto">CurrentFlowsTo</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentframeworkid">CurrentFrameworkId</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currenthaskeyboardfocus">CurrentHasKeyboardFocus</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext">CurrentHelpText</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement">CurrentIsContentElement</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement">CurrentIsControlElement</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentisdatavalidforform">CurrentIsDataValidForForm</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentisenabled">CurrentIsEnabled</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentiskeyboardfocusable">CurrentIsKeyboardFocusable</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentisoffscreen">CurrentIsOffscreen</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentispassword">CurrentIsPassword</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentisrequiredforform">CurrentIsRequiredForForm</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentitemstatus">CurrentItemStatus</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentitemtype">CurrentItemType</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentlabeledby">CurrentLabeledBy</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentlocalizedcontroltype">CurrentLocalizedControlType</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentname">CurrentName</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentnativewindowhandle">CurrentNativeWindowHandle</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentorientation">CurrentOrientation</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentprocessid">CurrentProcessId</a>


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

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentproviderdescription">CurrentProviderDescription</a>


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

<a href="/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>