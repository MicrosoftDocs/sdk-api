---
UID: NN:uiautomationcore.IGridProvider
title: IGridProvider (uiautomationcore.h)

description: Provides access to controls that act as containers for a collection of child elements organized in a two-dimensional logical coordinate system that can be traversed (that is, a Microsoft UI Automation client can move to adjacent controls) by using the keyboard.
old-location: winauto\uiauto_IGridProvider.htm
tech.root: WinAuto
ms.assetid: 37e2cc95-d765-4c2c-ae8a-5a072a43ad5a

ms.date: 12/05/2018
ms.keywords: IGridProvider, IGridProvider interface [Windows Accessibility], IGridProvider interface [Windows Accessibility],described, uiauto.uiauto_IGridProvider, uiauto_IGridProvider, uiautomationcore/IGridProvider, winauto.uiauto_IGridProvider
ms.topic: interface
f1_keywords: 
 - "uiautomationcore/IGridProvider"
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
 - IGridProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGridProvider interface


## -description


Provides access to 
        controls that act as containers for a collection of child elements organized in a two-dimensional 
        logical coordinate system that can be traversed (that is, a Microsoft UI Automation client can 
        move to adjacent controls) by using the keyboard. The children of this 
        element must implement <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-igriditemprovider">IGridItemProvider</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGridProvider</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGridProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGridProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-igridprovider-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Retrieves the UI Automation provider for the specified cell.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGridProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-igridprovider-get_columncount">ColumnCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the total number of columns in the grid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-igridprovider-get_rowcount">RowCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Specifies the total number of rows in the grid.

</td>
</tr>
</table> 


## -remarks



The <b>IGridProvider</b> interface exposes methods and properties to support UI Automation client access to controls 
		that act as containers for a collection of child elements. The children of this element must implement <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-igriditemprovider">IGridItemProvider</a>and be organized in a two-dimensional logical coordinate system that can be traversed (that is, a UI Automation client can move to adjacent controls) by using the keyboard.
		

Implemented on a UI Automation provider that must support 
        the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-implementinggrid">Grid</a> control pattern.

<b>IGridProvider</b> does not enable active manipulation of a grid; 
        <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider">ITransformProvider</a> must be implemented for this.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

