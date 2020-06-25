---
UID: NN:msrdc.ISimilarityFileIdTable
title: ISimilarityFileIdTable (msrdc.h)
description: Defines methods for storing and retrieving similarity file ID information.
helpviewer_keywords: ["ISimilarityFileIdTable","ISimilarityFileIdTable interface [Remote Differential Compression]","ISimilarityFileIdTable interface [Remote Differential Compression]","described","fs.isimilarityfileidtable","msrdc/ISimilarityFileIdTable","rdc.isimilarityfileidtable"]
old-location: rdc\isimilarityfileidtable.htm
tech.root: rdc
ms.assetid: 539a2e9b-9719-4012-bb7f-4d14723a3695
ms.date: 12/05/2018
ms.keywords: ISimilarityFileIdTable, ISimilarityFileIdTable interface [Remote Differential Compression], ISimilarityFileIdTable interface [Remote Differential Compression],described, fs.isimilarityfileidtable, msrdc/ISimilarityFileIdTable, rdc.isimilarityfileidtable
f1_keywords:
- msrdc/ISimilarityFileIdTable
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- MsRdc.dll
api_name:
- ISimilarityFileIdTable
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISimilarityFileIdTable interface


## -description


Defines methods for storing and retrieving similarity file ID information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimilarityFileIdTable</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISimilarityFileIdTable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISimilarityFileIdTable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityfileidtable-append">Append</a>
</td>
<td align="left" width="63%">
Adds a file ID to a similarity file ID table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityfileidtable-closetable">CloseTable</a>
</td>
<td align="left" width="63%">
Closes a similarity file ID table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityfileidtable-createtable">CreateTable</a>
</td>
<td align="left" width="63%">
Creates or opens a similarity file ID table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityfileidtable-createtableindirect">CreateTableIndirect</a>
</td>
<td align="left" width="63%">
Creates or opens a similarity file ID table using the RDC application's implementation of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilewriter">IRdcFileWriter</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityfileidtable-getrecordcount">GetRecordCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of records that are stored in a similarity file ID table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityfileidtable-invalidate">Invalidate</a>
</td>
<td align="left" width="63%">
Marks a file ID as not valid in the similarity file ID table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarityfileidtable-lookup">Lookup</a>
</td>
<td align="left" width="63%">
Retrieves the file ID in the similarity file ID table that corresponds to a given file index.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

