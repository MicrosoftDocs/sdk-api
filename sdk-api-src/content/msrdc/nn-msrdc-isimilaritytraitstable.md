---
UID: NN:msrdc.ISimilarityTraitsTable
title: ISimilarityTraitsTable (msrdc.h)
description: Defines methods for storing per-file similarity data and performing similarity lookups.
helpviewer_keywords: ["ISimilarityTraitsTable","ISimilarityTraitsTable interface [Remote Differential Compression]","ISimilarityTraitsTable interface [Remote Differential Compression]","described","fs.isimilaritytraitstable","msrdc/ISimilarityTraitsTable","rdc.isimilaritytraitstable"]
old-location: rdc\isimilaritytraitstable.htm
tech.root: rdc
ms.assetid: 0985e27c-aa70-43c1-bcec-00ef14f2df58
ms.date: 12/05/2018
ms.keywords: ISimilarityTraitsTable, ISimilarityTraitsTable interface [Remote Differential Compression], ISimilarityTraitsTable interface [Remote Differential Compression],described, fs.isimilaritytraitstable, msrdc/ISimilarityTraitsTable, rdc.isimilaritytraitstable
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISimilarityTraitsTable
 - msrdc/ISimilarityTraitsTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarityTraitsTable
---

# ISimilarityTraitsTable interface


## -description

Defines methods for storing per-file similarity data and performing similarity lookups.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimilarityTraitsTable</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISimilarityTraitsTable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISimilarityTraitsTable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilaritytraitstable-append">Append</a>
</td>
<td align="left" width="63%">
Adds a <a href="/windows/win32/api/msrdc/ns-msrdc-similaritydata">SimilarityData</a> structure to the similarity traits table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilaritytraitstable-begindump">BeginDump</a>
</td>
<td align="left" width="63%">
Retrieves similarity data from the similarity traits table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilaritytraitstable-closetable">CloseTable</a>
</td>
<td align="left" width="63%">
Closes a similarity traits table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilaritytraitstable-createtable">CreateTable</a>
</td>
<td align="left" width="63%">
Creates or opens a similarity traits table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilaritytraitstable-createtableindirect">CreateTableIndirect</a>
</td>
<td align="left" width="63%">
Creates or opens a similarity traits table using the RDC application's implementation of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msrdc/nf-msrdc-isimilaritytraitstable-findsimilarfileindex">FindSimilarFileIndex</a>
</td>
<td align="left" width="63%">
Returns a list of files that are similar to a given file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msrdc/nf-msrdc-isimilaritytraitstable-getlastindex">GetLastIndex</a>
</td>
<td align="left" width="63%">
Retrieves the index of the last entry that was stored in the similarity traits table.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

