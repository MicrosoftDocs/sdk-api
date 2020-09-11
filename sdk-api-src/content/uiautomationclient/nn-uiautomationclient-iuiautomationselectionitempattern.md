---
UID: NN:uiautomationclient.IUIAutomationSelectionItemPattern
title: IUIAutomationSelectionItemPattern (uiautomationclient.h)
description: Provides access to the selectable child items of a container control that supports IUIAutomationSelectionPattern.
helpviewer_keywords: ["IUIAutomationSelectionItemPattern","IUIAutomationSelectionItemPattern interface [Windows Accessibility]","IUIAutomationSelectionItemPattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationSelectionItemPattern","uiauto_IUIAutomationSelectionItemPattern","uiautomationclient/IUIAutomationSelectionItemPattern","winauto.uiauto_IUIAutomationSelectionItemPattern"]
old-location: winauto\uiauto_IUIAutomationSelectionItemPattern.htm
tech.root: WinAuto
ms.assetid: b76d5003-b9af-4a48-91d3-8075f45cf131
ms.date: 12/05/2018
ms.keywords: IUIAutomationSelectionItemPattern, IUIAutomationSelectionItemPattern interface [Windows Accessibility], IUIAutomationSelectionItemPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationSelectionItemPattern, uiauto_IUIAutomationSelectionItemPattern, uiautomationclient/IUIAutomationSelectionItemPattern, winauto.uiauto_IUIAutomationSelectionItemPattern
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
 - IUIAutomationSelectionItemPattern
 - uiautomationclient/IUIAutomationSelectionItemPattern
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
 - IUIAutomationSelectionItemPattern
---

# IUIAutomationSelectionItemPattern interface


## -description

Provides access to the selectable child items of a container control that supports <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationselectionpattern">IUIAutomationSelectionPattern</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationSelectionItemPattern</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationSelectionItemPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationSelectionItemPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection">AddToSelection</a>
</td>
<td align="left" width="63%">
Adds the current element to the collection of selected items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection">RemoveFromSelection</a>
</td>
<td align="left" width="63%">
Removes this element from the selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionitempattern-select">Select</a>
</td>
<td align="left" width="63%">
Clears any selected items and then selects the current element.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationSelectionItemPattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionitempattern-get_cachedisselected">CachedIsSelected</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
A cached value that indicates whether this item is selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionitempattern-get_cachedselectioncontainer">CachedSelectionContainer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached element that supports <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationselectionpattern">IUIAutomationSelectionPattern</a> and acts as the container for this item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionitempattern-get_currentisselected">CurrentIsSelected</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether this item is selected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionitempattern-get_currentselectioncontainer">CurrentSelectionContainer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the element that supports <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationselectionpattern">IUIAutomationSelectionPattern</a> and acts as the container for this item.



</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>

