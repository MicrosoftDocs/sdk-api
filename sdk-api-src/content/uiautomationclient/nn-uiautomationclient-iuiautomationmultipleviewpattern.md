---
UID: NN:uiautomationclient.IUIAutomationMultipleViewPattern
title: IUIAutomationMultipleViewPattern (uiautomationclient.h)
description: Provides access to a control that can switch between multiple representations of the same information or set of child controls.helpviewer_keywords: ["IUIAutomationMultipleViewPattern","IUIAutomationMultipleViewPattern interface [Windows Accessibility]","IUIAutomationMultipleViewPattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationMultipleViewPattern","uiauto_IUIAutomationMultipleViewPattern","uiautomationclient/IUIAutomationMultipleViewPattern","winauto.uiauto_IUIAutomationMultipleViewPattern"]
old-location: winauto\uiauto_IUIAutomationMultipleViewPattern.htm
tech.root: WinAuto
ms.assetid: 4a1613b9-1e64-4d4e-876e-e2bf886097d4
ms.date: 12/05/2018
ms.keywords: IUIAutomationMultipleViewPattern, IUIAutomationMultipleViewPattern interface [Windows Accessibility], IUIAutomationMultipleViewPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationMultipleViewPattern, uiauto_IUIAutomationMultipleViewPattern, uiautomationclient/IUIAutomationMultipleViewPattern, winauto.uiauto_IUIAutomationMultipleViewPattern
f1_keywords:
- uiautomationclient/IUIAutomationMultipleViewPattern
dev_langs:
- c++
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
- IUIAutomationMultipleViewPattern
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationMultipleViewPattern interface


## -description


Provides access to a control that  can switch between multiple representations of the same information or set of child controls.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationMultipleViewPattern</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationMultipleViewPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationMultipleViewPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationmultipleviewpattern-getcachedsupportedviews">GetCachedSupportedViews</a>
</td>
<td align="left" width="63%">
Retrieves a collection of control-specific view identifiers from the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationmultipleviewpattern-getcurrentsupportedviews">GetCurrentSupportedViews</a>
</td>
<td align="left" width="63%">
Retrieves a collection of control-specific view identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationmultipleviewpattern-getviewname">GetViewName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a control-specific view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationmultipleviewpattern-setcurrentview">SetCurrentView</a>
</td>
<td align="left" width="63%">
Sets the view of the control.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationMultipleViewPattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationmultipleviewpattern-get_cachedcurrentview">CachedCurrentView</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached control-specific identifier of the current view of the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationmultipleviewpattern-get_currentcurrentview">CurrentCurrentView</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the control-specific identifier of the current view of the control.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
 

 

