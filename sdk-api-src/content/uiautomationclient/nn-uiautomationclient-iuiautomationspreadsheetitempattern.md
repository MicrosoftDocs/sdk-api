---
UID: NN:uiautomationclient.IUIAutomationSpreadsheetItemPattern
title: IUIAutomationSpreadsheetItemPattern (uiautomationclient.h)
author: windows-sdk-content
description: Enables a client application to retrieve information about an item (cell) in a spreadsheet.
old-location: winauto\uiauto_IUIAutomationSpreadsheetItemPattern.htm
tech.root: WinAuto
ms.assetid: 4B90ED28-5F85-4F36-8F11-1F2B60CEC9E5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomationSpreadsheetItemPattern, IUIAutomationSpreadsheetItemPattern interface [Windows Accessibility], IUIAutomationSpreadsheetItemPattern interface [Windows Accessibility],described, uiautomationclient/IUIAutomationSpreadsheetItemPattern, winauto.uiauto_IUIAutomationSpreadsheetItemPattern
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
 - IUIAutomationSpreadsheetItemPattern
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationSpreadsheetItemPattern interface


## -description


Enables a client application to retrieve information about an item (cell) in a spreadsheet.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationSpreadsheetItemPattern</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationSpreadsheetItemPattern</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUIAutomationSpreadsheetItemPattern</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcachedannotationobjects">GetCachedAnnotationObjects</a>
</td>
<td align="left" width="63%">
Retrieves a cached array of elements representing the annotations associated with this spreadsheet cell. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcachedannotationtypes">GetCachedAnnotationTypes</a>
</td>
<td align="left" width="63%">
Retrieves a cached array of annotation type identifiers indicating the types of annotations that are associated with this spreadsheet cell. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcurrentannotationobjects">GetCurrentAnnotationObjects</a>
</td>
<td align="left" width="63%">
Retrieves an array of elements representing the annotations associated with this spreadsheet cell. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-getcurrentannotationtypes">GetCurrentAnnotationTypes</a>
</td>
<td align="left" width="63%">
Retrieves an array of annotation type identifiers indicating the types of annotations that are associated with this spreadsheet cell.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAutomationSpreadsheetItemPattern</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-get_cachedformula">CachedFormula</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the cached formula for this cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetitempattern-get_currentformula">CurrentFormula</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the formula for this cell.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
 

 

