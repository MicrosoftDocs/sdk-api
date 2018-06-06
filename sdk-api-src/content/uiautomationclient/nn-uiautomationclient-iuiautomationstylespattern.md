---
UID: NN:uiautomationclient.IUIAutomationStylesPattern
title: IUIAutomationStylesPattern
author: windows-sdk-content
description: Enables Microsoft UI Automation clients to retrieve the visual styles associated with an element in a document.
old-location: winauto\uiauto_IUIAutomationStylesPattern.htm
old-project: WinAuto
ms.assetid: 83529CFD-46D2-45A7-9B0D-F00FF43D911B
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: IUIAutomationStylesPattern, IUIAutomationStylesPattern interface [Windows Accessibility], IUIAutomationStylesPattern interface [Windows Accessibility],described, uiautomationclient/IUIAutomationStylesPattern, winauto.uiauto_IUIAutomationStylesPattern
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IUIAutomationStylesPattern
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationStylesPattern interface


## -description


Enables Microsoft UI Automation clients to retrieve the visual styles associated with an element in a document.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationStylesPattern</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAutomationStylesPattern</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/D284E4B6-A328-4D79-A95F-DACE00042AF2">GetCachedExtendedPropertiesArray </a>
</td>
<td align="left" width="63%">
Retrieves the cached extended properties for an element in a document.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AA128739-FB03-4E68-904B-648AE34A175C">GetCurrentExtendedPropertiesArray </a>
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

<a href="https://msdn.microsoft.com/79B9AFBF-EAA2-45F6-B027-C12F0B4B4CCC">CachedExtendedProperties</a>


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

<a href="https://msdn.microsoft.com/6623D66E-E79C-4E50-BC5F-B2B226B1FC65">CachedFillColor</a>


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

<a href="https://msdn.microsoft.com/7977770D-1B61-4FE7-846B-C4EE6A0647EE">CachedFillPatternColor</a>


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

<a href="https://msdn.microsoft.com/DB6D21C8-ADF3-4640-9B46-59033F015A22">CachedShape</a>


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

<a href="https://msdn.microsoft.com/F884A9FF-4538-41B6-A067-246A8897F076">CachedStyleId</a>


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

<a href="https://msdn.microsoft.com/FFFD7437-842E-42FC-99A0-27E2EFA9F645">CachedStyleName</a>


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

<a href="https://msdn.microsoft.com/E0D643A5-92C5-4307-88A9-8CC13903D976">CurrentExtendedProperties</a>


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

<a href="https://msdn.microsoft.com/3B1C3731-72E5-4407-AFA8-4E5ACB3F1FD2">CurrentFillColor</a>


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

<a href="https://msdn.microsoft.com/38CFF0E5-D96D-4FA3-86B1-581DC5E7F1F3">CurrentFillPatternColor</a>


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

<a href="https://msdn.microsoft.com/597609F0-D2F1-447D-80EC-426066581380">CurrentShape</a>


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

<a href="https://msdn.microsoft.com/0A27D032-5FC2-4095-A454-C1D6E7255D2A">CurrentStyleId</a>


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

<a href="https://msdn.microsoft.com/008044D6-9B7B-4E1B-B22D-7518C830E4D2">CurrentStyleName</a>


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




<a href="https://msdn.microsoft.com/14358ef0-aa54-42c1-a3da-0f835f5f5ef6">Control Pattern Interfaces for Clients</a>
 

 

