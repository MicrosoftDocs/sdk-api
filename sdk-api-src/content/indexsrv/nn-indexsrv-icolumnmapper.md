---
UID: NN:indexsrv.IColumnMapper
title: IColumnMapper
author: windows-sdk-content
description: Retrieves property information for file based queries.
old-location: search\icolumnmapper.htm
tech.root: search
ms.assetid: CBC7EE6C-299D-4B9D-839A-0A2755CA8112
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IColumnMapper, IColumnMapper interface [search], IColumnMapper interface [search],described, indexsrv/IColumnMapper, search.icolumnmapper
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: indexsrv.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - indexsrv.h
api_name:
 - IColumnMapper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IColumnMapper interface


## -description


Retrieves property information for file based queries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IColumnMapper</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IColumnMapper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IColumnMapper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E24E7258-1A5D-4FA0-8F17-6E2B00582AF3">EnumPropInfo</a>
</td>
<td align="left" width="63%">
Gets the i-th entry from the list of properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94E7A6B4-0EA9-40F4-B69B-B1A30B0B5229">GetPropInfoFromId</a>
</td>
<td align="left" width="63%">
Gets the property information from the DBID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F9306234-7CCC-412E-AA8C-7E8A04A8132F">GetPropInfoFromName</a>
</td>
<td align="left" width="63%">
Gets property information from a name. This will return a DBID pointer in parameter <i>ppPropId</i> which now has to be freed by the caller and not by the callee (this class).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B6B47014-CAAD-40B3-8A39-A81AD40AE1D2">IsMapUpToDate</a>
</td>
<td align="left" width="63%">
Determines if the map is up to date.

</td>
</tr>
</table> 

