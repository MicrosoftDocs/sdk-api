---
UID: NN:uiautomationclient.IUIAutomationSelectionPattern
title: IUIAutomationSelectionPattern (uiautomationclient.h)

description: Provides access to a control that contains selectable child items. The children of this element support IUIAutomationSelectionItemPattern.
old-location: winauto\uiauto_IUIAutomationSelectionPattern.htm
tech.root: WinAuto
ms.assetid: 10e0c9c3-ed42-4ffa-b0a8-25a1c760a583

ms.date: 12/05/2018
ms.keywords: IUIAutomationSelectionPattern, IUIAutomationSelectionPattern interface [Windows Accessibility], IUIAutomationSelectionPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationSelectionPattern, uiauto_IUIAutomationSelectionPattern, uiautomationclient/IUIAutomationSelectionPattern, winauto.uiauto_IUIAutomationSelectionPattern
ms.topic: interface
f1_keywords: 
 - "uiautomationclient/IUIAutomationSelectionPattern"
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
 - IUIAutomationSelectionPattern
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationSelectionPattern interface


## -description


Provides access to a control that contains selectable child items. The children of this element support <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationselectionitempattern">IUIAutomationSelectionItemPattern</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationSelectionPattern</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationSelectionPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationSelectionPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionpattern-getcachedselection">GetCachedSelection</a>
</td>
<td align="left" width="63%">
Retrieves the cached selected elements in the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionpattern-getcurrentselection">GetCurrentSelection</a>
</td>
<td align="left" width="63%">
Retrieves the selected elements in the container.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationSelectionPattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionpattern-get_cachedcanselectmultiple">CachedCanSelectMultiple</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether more than one item in the container can be selected at one time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionpattern-get_cachedisselectionrequired">CachedIsSelectionRequired</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a cached value that indicates whether at least one item must be selected at all times.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionpattern-get_currentcanselectmultiple">CurrentCanSelectMultiple</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether more than one item in the container can be selected at one time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionpattern-get_currentisselectionrequired">CurrentIsSelectionRequired</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether at least one item must be selected at all times.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
 

 

