---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITableItemProvider interface


## -description


Provides access 
        to child controls of containers that implement <a href="https://msdn.microsoft.com/ae6be8be-78ea-4843-924f-2dc5d5286da2">ITableProvider</a>. 
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITableItemProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITableItemProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITableItemProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b08e20e8-142c-4f83-8422-c0e6ae2b7ebf">GetColumnHeaderItems</a>
</td>
<td align="left" width="63%">

        Retrieves a collection of UI Automation provider 
        representing all the column headers associated with a table item or cell.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02717f9a-93dd-4963-bbc7-a1eb257bf5e5">GetRowHeaderItems</a>
</td>
<td align="left" width="63%">

        Retrieves a collection of UI Automation provider 
        representing all the row headers associated with a table item or cell.
        

</td>
</tr>
</table> 


## -remarks




            This control pattern is analogous to <a href="https://msdn.microsoft.com/334a10f1-8bfc-4935-9eee-6176a3e8a4f1">IGridItemProvider</a> with 
            the distinction that any control implementing <b>ITableItemProvider</b> 
            must expose the relationship between the individual cell and its row and column information.
            


            Access to individual cell functionality is provided by the concurrent implementation 
            of <a href="https://msdn.microsoft.com/334a10f1-8bfc-4935-9eee-6176a3e8a4f1">IGridItemProvider</a>. 
            


            Implemented on a UI Automation provider that must 
            support the <a href="https://msdn.microsoft.com/e00c7a58-410c-4818-8f61-57ee98527d6e">TableItem</a> control pattern.
            




## -see-also




<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

