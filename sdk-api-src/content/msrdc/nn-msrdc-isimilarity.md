---
UID: NN:msrdc.ISimilarity
title: ISimilarity (msrdc.h)
author: windows-sdk-content
description: Defines methods for storing and retrieving per-file similarity data and file IDs in a similarity file.
old-location: rdc\isimilarity.htm
tech.root: rdc
ms.assetid: fe0cd874-a40c-4d82-99bf-b84008a4995c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISimilarity, ISimilarity interface [Remote Differential Compression], ISimilarity interface [Remote Differential Compression],described, fs.isimilarity, msrdc/ISimilarity, rdc.isimilarity
ms.topic: interface
f1_keywords: 
 - "msrdc/ISimilarity"
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
 - ISimilarity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISimilarity interface


## -description


Defines methods for storing and retrieving per-file similarity data and file IDs  in a similarity file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimilarity</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISimilarity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISimilarity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-append">Append</a>
</td>
<td align="left" width="63%">
Adds the file ID and similarity data information to the tables in the similarity file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-closetable">CloseTable</a>
</td>
<td align="left" width="63%">
Closes the tables in a similarity file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-copyandswap">CopyAndSwap</a>
</td>
<td align="left" width="63%">
Creates copies of an existing similarity traits table and an existing similarity file ID table, swaps the internal pointers, and deletes the existing tables.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-createtable">CreateTable</a>
</td>
<td align="left" width="63%">
Creates or opens a similarity traits table and a similarity file ID table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-createtableindirect">CreateTableIndirect</a>
</td>
<td align="left" width="63%">
Creates or opens a similarity traits table and a similarity file ID table using the RDC application's implementations of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilewriter">IRdcFileWriter</a> interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-findsimilarfileid">FindSimilarFileId</a>
</td>
<td align="left" width="63%">
Returns a list of files that are similar to a given file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msrdc/nf-msrdc-isimilarity-getrecordcount">GetRecordCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of records that are stored in the similarity file ID table in a similarity file.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

