---
UID: NN:uiautomationclient.IUIAutomationGridPattern
title: IUIAutomationGridPattern (uiautomationclient.h)
description: Provides access to a control that acts as a container for a collection of child controls that are organized in a two-dimensional logical coordinate system that can be traversed by row and column.
helpviewer_keywords: ["IUIAutomationGridPattern","IUIAutomationGridPattern interface [Windows Accessibility]","IUIAutomationGridPattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationGridPattern","uiauto_IUIAutomationGridPattern","uiautomationclient/IUIAutomationGridPattern","winauto.uiauto_IUIAutomationGridPattern"]
old-location: winauto\uiauto_IUIAutomationGridPattern.htm
tech.root: WinAuto
ms.assetid: 36a4893e-5f49-413c-a29a-e58291c7d057
ms.date: 12/05/2018
ms.keywords: IUIAutomationGridPattern, IUIAutomationGridPattern interface [Windows Accessibility], IUIAutomationGridPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationGridPattern, uiauto_IUIAutomationGridPattern, uiautomationclient/IUIAutomationGridPattern, winauto.uiauto_IUIAutomationGridPattern
f1_keywords:
- uiautomationclient/IUIAutomationGridPattern
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
- IUIAutomationGridPattern
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationGridPattern interface


## -description


Provides access to  a control that acts as a container for a collection of child controls that  are organized in a two-dimensional logical coordinate system that can be traversed by row and column. The children of this element support the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationgriditempattern">IUIAutomationGridItemPattern</a> interface. 
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationGridPattern</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationGridPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationGridPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationgridpattern-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Retrieves a UI Automation element representing an item in the grid.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationGridPattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationgridpattern-get_cachedcolumncount">CachedColumnCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached number of columns in the grid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationgridpattern-get_cachedrowcount">CachedRowCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached number of rows in the grid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationgridpattern-get_currentcolumncount">CurrentColumnCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The number of columns in the grid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationgridpattern-get_currentrowcount">CurrentRowCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of rows in the grid.

</td>
</tr>
</table> 


## -remarks



This interface does not support active manipulation of a grid; the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtransformpattern">IUIAutomationTransformPattern</a> interface is required for this functionality. 
            




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
 

 

