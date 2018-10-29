---
UID: NN:uiautomationcore.IGridProvider
title: IGridProvider
author: windows-sdk-content
description: Provides access to controls that act as containers for a collection of child elements organized in a two-dimensional logical coordinate system that can be traversed (that is, a Microsoft UI Automation client can move to adjacent controls) by using the keyboard.
old-location: winauto\uiauto_IGridProvider.htm
tech.root: WinAuto
ms.assetid: 37e2cc95-d765-4c2c-ae8a-5a072a43ad5a
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IGridProvider, IGridProvider interface [Windows Accessibility], IGridProvider interface [Windows Accessibility],described, uiauto.uiauto_IGridProvider, uiauto_IGridProvider, uiautomationcore/IGridProvider, winauto.uiauto_IGridProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGridProvider interface


## -description


Provides access to 
        controls that act as containers for a collection of child elements organized in a two-dimensional 
        logical coordinate system that can be traversed (that is, a Microsoft UI Automation client can 
        move to adjacent controls) by using the keyboard. The children of this 
        element must implement <a href="https://msdn.microsoft.com/334a10f1-8bfc-4935-9eee-6176a3e8a4f1">IGridItemProvider</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGridProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGridProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5d62e872-c4a7-43c5-b5cf-5069ad46483a">GetItem</a>
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

<a href="https://msdn.microsoft.com/8d180781-d797-4db4-82bd-92f3646da495">ColumnCount</a>


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

<a href="https://msdn.microsoft.com/036a05fd-53b7-4e6d-b96b-503832933b56">RowCount</a>


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
		that act as containers for a collection of child elements. The children of this element must implement <a href="https://msdn.microsoft.com/334a10f1-8bfc-4935-9eee-6176a3e8a4f1">IGridItemProvider</a>and be organized in a two-dimensional logical coordinate system that can be traversed (that is, a UI Automation client can move to adjacent controls) by using the keyboard.
		

Implemented on a UI Automation provider that must support 
        the <a href="https://msdn.microsoft.com/c50fb6f7-884a-4147-a6b2-c59d787fc04b">Grid</a> control pattern.

<b>IGridProvider</b> does not enable active manipulation of a grid; 
        <a href="https://msdn.microsoft.com/cdc2f81b-cf69-469f-9139-e9a73cf8c730">ITransformProvider</a> must be implemented for this.




## -see-also




<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

