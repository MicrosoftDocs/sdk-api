---
UID: NN:indexsrv.IColumnMapper
title: IColumnMapper (indexsrv.h)

description: Retrieves property information for file based queries.
old-location: search\icolumnmapper.htm
tech.root: search
ms.assetid: CBC7EE6C-299D-4B9D-839A-0A2755CA8112

ms.date: 12/05/2018
ms.keywords: IColumnMapper, IColumnMapper interface [search], IColumnMapper interface [search],described, indexsrv/IColumnMapper, search.icolumnmapper
ms.topic: interface
f1_keywords: 
 - "indexsrv/IColumnMapper"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IColumnMapper interface


## -description


Retrieves property information for file based queries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IColumnMapper</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IColumnMapper</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nf-indexsrv-icolumnmapper-enumpropinfo">EnumPropInfo</a>
</td>
<td align="left" width="63%">
Gets the i-th entry from the list of properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nf-indexsrv-icolumnmapper-getpropinfofromid">GetPropInfoFromId</a>
</td>
<td align="left" width="63%">
Gets the property information from the DBID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nf-indexsrv-icolumnmapper-getpropinfofromname">GetPropInfoFromName</a>
</td>
<td align="left" width="63%">
Gets property information from a name. This will return a DBID pointer in parameter <i>ppPropId</i> which now has to be freed by the caller and not by the callee (this class).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nf-indexsrv-icolumnmapper-ismapuptodate">IsMapUpToDate</a>
</td>
<td align="left" width="63%">
Determines if the map is up to date.

</td>
</tr>
</table> 

