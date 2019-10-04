---
UID: NN:uiautomationclient.IUIAutomationStylesPattern
title: IUIAutomationStylesPattern (uiautomationclient.h)
author: windows-sdk-content
description: Enables Microsoft UI Automation clients to retrieve the visual styles associated with an element in a document.
old-location: winauto\uiauto_IUIAutomationStylesPattern.htm
tech.root: WinAuto
ms.assetid: 83529CFD-46D2-45A7-9B0D-F00FF43D911B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomationStylesPattern, IUIAutomationStylesPattern interface [Windows Accessibility], IUIAutomationStylesPattern interface [Windows Accessibility],described, uiautomationclient/IUIAutomationStylesPattern, winauto.uiauto_IUIAutomationStylesPattern
ms.topic: interface
f1_keywords: 
 - "uiautomationclient/IUIAutomationStylesPattern"
dev_langs:
 - c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IUIAutomationStylesPattern
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationStylesPattern interface


## -description


Enables Microsoft UI Automation clients to retrieve the visual styles associated with an element in a document.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationStylesPattern</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationStylesPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationStylesPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437294(v=vs.85)">GetCachedExtendedPropertiesArray </a>
</td>
<td align="left" width="63%">
Retrieves the cached extended properties for an element in a document.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437295(v=vs.85)">GetCurrentExtendedPropertiesArray </a>
</td>
<td align="left" width="63%">
Retrieves the extended properties for an element in a document.



</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationStylesPattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationstylespattern-get_cachedextendedproperties">CachedExtendedProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached localized string that contains the list of extended properties for an element in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationstylespattern-get_cachedfillcolor">CachedFillColor</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached fill color of an element in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationstylespattern-get_cachedfillpatterncolor">CachedFillPatternColor</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached color of the pattern used to fill an element in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationstylespattern-get_cachedshape">CachedShape</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached shape of an element in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationstylespattern-get_cachedstyleid">CachedStyleId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached identifier of the visual style associated with an element in a document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationstylespattern-get_cachedstylename">CachedStyleName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached name of the visual style associated with an element in a document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationstylespattern-get_currentextendedproperties">CurrentExtendedProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a localized string that contains the list of extended properties for an element in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationstylespattern-get_currentfillcolor">CurrentFillColor</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the fill color of an element in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationstylespattern-get_currentfillpatterncolor">CurrentFillPatternColor</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the color of the pattern used to fill an element in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationstylespattern-get_currentshape">CurrentShape</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the shape of an element in a document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationstylespattern-get_currentstyleid">CurrentStyleId</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the identifier of the visual style associated with an element in a document. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationstylespattern-get_currentstylename">CurrentStyleName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of the visual style associated with an element in a document. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
 

 

