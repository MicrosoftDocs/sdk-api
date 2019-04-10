---
UID: NN:uiautomationcore.ISpreadsheetItemProvider
title: ISpreadsheetItemProvider (uiautomationcore.h)
author: windows-sdk-content
description: Provides access to information about an item (cell) in a spreadsheet.
old-location: winauto\uiauto_ISpreadsheetItemProvider.htm
tech.root: WinAuto
ms.assetid: E6428FED-2BCC-4AD5-B612-A22899624538
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISpreadsheetItemProvider, ISpreadsheetItemProvider interface [Windows Accessibility], ISpreadsheetItemProvider interface [Windows Accessibility],described, uiautomationcore/ISpreadsheetItemProvider, winauto.uiauto_ISpreadsheetItemProvider
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - ISpreadsheetItemProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpreadsheetItemProvider interface


## -description


Provides access 
        to information about an item (cell) in a spreadsheet. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpreadsheetItemProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpreadsheetItemProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ISpreadsheetItemProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5B9BDAF8-A7A7-492B-97F7-8502E630203F">GetAnnotationObjects</a>
</td>
<td align="left" width="63%">
Retrieves an array of objects that represent the annotations associated with this spreadsheet cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95DD80C7-AD98-42D5-BB2E-05ACA02F878A">GetAnnotationTypes</a>
</td>
<td align="left" width="63%">
Retrieves an array of annotation type identifiers indicating the types of annotations that are associated with this spreadsheet cell. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpreadsheetItemProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/525A187A-0CAB-479C-9A04-03E231CC10EE">Formula</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the formula for this spreadsheet cell.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/08d0226d-845c-4564-a059-539b62fc7909">Control Pattern Interfaces for Providers</a>
 

 

