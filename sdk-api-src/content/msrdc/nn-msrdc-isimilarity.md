---
UID: NN:msrdc.ISimilarity
title: ISimilarity
author: windows-sdk-content
description: Defines methods for storing and retrieving per-file similarity data and file IDs in a similarity file.
old-location: rdc\isimilarity.htm
old-project: Rdc
ms.assetid: fe0cd874-a40c-4d82-99bf-b84008a4995c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISimilarity, ISimilarity interface [Remote Differential Compression], ISimilarity interface [Remote Differential Compression],described, fs.isimilarity, msrdc/ISimilarity, rdc.isimilarity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msrdc.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RdcMappingAccessMode
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
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarity interface


## -description


Defines methods for storing and retrieving per-file similarity data and file IDs  in a similarity file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimilarity</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISimilarity</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f8896d9e-ca6a-404f-b80f-ef739ec97b53">Append</a>
</td>
<td align="left" width="63%">
Adds the file ID and similarity data information to the tables in the similarity file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bf16568-ed61-42a3-91b9-79a1aa731bc0">CloseTable</a>
</td>
<td align="left" width="63%">
Closes the tables in a similarity file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a31530e-da6d-4ac8-9fd4-d91419777ce5">CopyAndSwap</a>
</td>
<td align="left" width="63%">
Creates copies of an existing similarity traits table and an existing similarity file ID table, swaps the internal pointers, and deletes the existing tables.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/808c20f9-054d-475d-8ca3-ee2dde871426">CreateTable</a>
</td>
<td align="left" width="63%">
Creates or opens a similarity traits table and a similarity file ID table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84df73f5-0c39-44bd-81d8-d5ca144eb2e8">CreateTableIndirect</a>
</td>
<td align="left" width="63%">
Creates or opens a similarity traits table and a similarity file ID table using the RDC application's implementations of the <a href="https://msdn.microsoft.com/1ddc599b-5a9b-4807-9005-00793f9a6ed4">ISimilarityTraitsMapping</a> and <a href="https://msdn.microsoft.com/8b6ac8d0-37fd-4bd3-aa44-5b57f546364d">IRdcFileWriter</a> interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70a205fc-d90a-43fc-88f4-2f3a573c5a82">FindSimilarFileId</a>
</td>
<td align="left" width="63%">
Returns a list of files that are similar to a given file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19dda0ed-0f11-4e17-823b-667a48cf6dc1">GetRecordCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of records that are stored in the similarity file ID table in a similarity file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

