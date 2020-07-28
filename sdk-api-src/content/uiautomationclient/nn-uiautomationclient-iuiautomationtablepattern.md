---
UID: NN:uiautomationclient.IUIAutomationTablePattern
title: IUIAutomationTablePattern (uiautomationclient.h)
description: Provides access to a control that acts as a container for a collection of child elements.
helpviewer_keywords: ["IUIAutomationTablePattern","IUIAutomationTablePattern interface [Windows Accessibility]","IUIAutomationTablePattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationTablePattern","uiauto_IUIAutomationTablePattern","uiautomationclient/IUIAutomationTablePattern","winauto.uiauto_IUIAutomationTablePattern"]
old-location: winauto\uiauto_IUIAutomationTablePattern.htm
tech.root: WinAuto
ms.assetid: a393b323-31f9-4f31-abdb-7a0fb7c8ab96
ms.date: 12/05/2018
ms.keywords: IUIAutomationTablePattern, IUIAutomationTablePattern interface [Windows Accessibility], IUIAutomationTablePattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationTablePattern, uiauto_IUIAutomationTablePattern, uiautomationclient/IUIAutomationTablePattern, winauto.uiauto_IUIAutomationTablePattern
f1_keywords:
- uiautomationclient/IUIAutomationTablePattern
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
- IUIAutomationTablePattern
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTablePattern interface


## -description


Provides access to a control that acts as a container for a collection of child elements. The children of this element support <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtableitempattern">IUIAutomationTableItemPattern</a> and are organized in a two-dimensional logical coordinate system that can be traversed by row and column.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTablePattern</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationTablePattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationTablePattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtablepattern-getcachedcolumnheaders">GetCachedColumnHeaders</a>
</td>
<td align="left" width="63%">
Retrieves a cached collection of UI Automation elements representing all the column headers in a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtablepattern-getcachedrowheaders">GetCachedRowHeaders</a>
</td>
<td align="left" width="63%">
Retrieves a cached collection of UI Automation elements representing all the row headers in a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtablepattern-getcurrentcolumnheaders">GetCurrentColumnHeaders</a>
</td>
<td align="left" width="63%">
Retrieves a collection of UI Automation elements representing all the column headers in a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtablepattern-getcurrentrowheaders">GetCurrentRowHeaders</a>
</td>
<td align="left" width="63%">
Retrieves a collection of UI Automation elements representing all the row headers in a table.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationTablePattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtablepattern-get_cachedroworcolumnmajor">CachedRowOrColumnMajor</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached primary direction of traversal for the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationtablepattern-get_currentroworcolumnmajor">CurrentRowOrColumnMajor</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the primary direction of traversal for the table.

</td>
</tr>
</table> 


## -remarks



This control pattern is analogous to <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationgridpattern">IUIAutomationGridPattern</a> with the distinction that any control that supports <b>IUIAutomationTablePattern</b> also exposes a column or row header relationship, or both, for each child element. Controls that support the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingtableitem">Table</a> control pattern also support the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementinggrid">Grid</a> control pattern in order to provide access to the inherent grid functionality of a table.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
 

 

