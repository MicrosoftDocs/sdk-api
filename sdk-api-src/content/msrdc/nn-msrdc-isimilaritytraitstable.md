---
UID: NN:msrdc.ISimilarityTraitsTable
title: ISimilarityTraitsTable (msrdc.h)
author: windows-sdk-content
description: Defines methods for storing per-file similarity data and performing similarity lookups.
old-location: rdc\isimilaritytraitstable.htm
tech.root: rdc
ms.assetid: 0985e27c-aa70-43c1-bcec-00ef14f2df58
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISimilarityTraitsTable, ISimilarityTraitsTable interface [Remote Differential Compression], ISimilarityTraitsTable interface [Remote Differential Compression],described, fs.isimilaritytraitstable, msrdc/ISimilarityTraitsTable, rdc.isimilaritytraitstable
ms.topic: interface
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
 - ISimilarityTraitsTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISimilarityTraitsTable interface


## -description


Defines methods for storing per-file similarity data and performing similarity lookups.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimilarityTraitsTable</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISimilarityTraitsTable</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e4c5f75c-282e-4c99-8c5a-53421f4bfc92">Append</a>
</td>
<td align="left" width="63%">
Adds a <a href="https://msdn.microsoft.com/33fdb48c-6f33-44e8-83b1-6029b1eace1d">SimilarityData</a> structure to the similarity traits table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93298019-334b-4685-b95e-a1081c2bd9dc">BeginDump</a>
</td>
<td align="left" width="63%">
Retrieves similarity data from the similarity traits table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/941f1e81-035d-4935-bcdf-8c9c6ad9ed4d">CloseTable</a>
</td>
<td align="left" width="63%">
Closes a similarity traits table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35fd9ea1-85bf-424c-b0e2-dcdfbb6940fb">CreateTable</a>
</td>
<td align="left" width="63%">
Creates or opens a similarity traits table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55bd485f-33f7-4247-bc13-f5e2c7e70028">CreateTableIndirect</a>
</td>
<td align="left" width="63%">
Creates or opens a similarity traits table using the RDC application's implementation of the <a href="https://msdn.microsoft.com/1ddc599b-5a9b-4807-9005-00793f9a6ed4">ISimilarityTraitsMapping</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09c9b918-1def-4d19-84d4-99b881070e36">FindSimilarFileIndex</a>
</td>
<td align="left" width="63%">
Returns a list of files that are similar to a given file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e6cb7b4-0dcf-4a51-acf9-3263d73eee63">GetLastIndex</a>
</td>
<td align="left" width="63%">
Retrieves the index of the last entry that was stored in the similarity traits table.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

