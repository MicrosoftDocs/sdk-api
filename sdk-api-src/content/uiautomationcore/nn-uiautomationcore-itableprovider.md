---
UID: NN:uiautomationcore.ITableProvider
title: ITableProvider (uiautomationcore.h)
description: Provides access to controls that act as containers for a collection of child elements.
helpviewer_keywords: ["ITableProvider","ITableProvider interface [Windows Accessibility]","ITableProvider interface [Windows Accessibility]","described","uiauto.uiauto_ITableProvider","uiauto_ITableProvider","uiautomationcore/ITableProvider","winauto.uiauto_ITableProvider"]
old-location: winauto\uiauto_ITableProvider.htm
tech.root: WinAuto
ms.assetid: ae6be8be-78ea-4843-924f-2dc5d5286da2
ms.date: 12/05/2018
ms.keywords: ITableProvider, ITableProvider interface [Windows Accessibility], ITableProvider interface [Windows Accessibility],described, uiauto.uiauto_ITableProvider, uiauto_ITableProvider, uiautomationcore/ITableProvider, winauto.uiauto_ITableProvider
f1_keywords:
- uiautomationcore/ITableProvider
dev_langs:
- c++
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
- ITableProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITableProvider interface


## -description


Provides access 
        to controls that act as containers for a collection of child elements. The children of 
        this element must implement <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itableitemprovider">ITableItemProvider</a> and be organized 
        in a two-dimensional logical coordinate system that can be traversed by using the keyboard.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITableProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITableProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITableProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itableprovider-getcolumnheaders">GetColumnHeaders</a>
</td>
<td align="left" width="63%">
Gets a collection of UI Automation providers 
        that represents all the column headers in a table.        
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itableprovider-getrowheaders">GetRowHeaders</a>
</td>
<td align="left" width="63%">
Gets a collection of UI Automation providers 
        that represents all the row headers in a table.        
        

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITableProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor">RowOrColumnMajor</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the primary direction of traversal for the table.

</td>
</tr>
</table> 


## -remarks



This control pattern is analogous to <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-igridprovider">IGridProvider</a> with 
            the distinction that any control that implements <b>ITableProvider</b> must 
            also expose a column and/or row header relationship for each child element.
            

Controls that implement <b>ITableProvider</b> are also required to 
            implement <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-igridprovider">IGridProvider</a> so as to expose the inherent grid functionality 
            of a table control.
            

         
            Implemented on a UI Automation provider that must support 
            the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementingtable">Table</a> control pattern and <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementinggrid">Grid</a> control pattern.
            




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

