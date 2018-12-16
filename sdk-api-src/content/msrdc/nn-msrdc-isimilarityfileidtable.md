---
UID: NN:msrdc.ISimilarityFileIdTable
title: ISimilarityFileIdTable
author: windows-sdk-content
description: Defines methods for storing and retrieving similarity file ID information.
old-location: rdc\isimilarityfileidtable.htm
tech.root: rdc
ms.assetid: 539a2e9b-9719-4012-bb7f-4d14723a3695
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISimilarityFileIdTable, ISimilarityFileIdTable interface [Remote Differential Compression], ISimilarityFileIdTable interface [Remote Differential Compression],described, fs.isimilarityfileidtable, msrdc/ISimilarityFileIdTable, rdc.isimilarityfileidtable
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
 - ISimilarityFileIdTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISimilarityFileIdTable interface


## -description


Defines methods for storing and retrieving similarity file ID information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimilarityFileIdTable</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISimilarityFileIdTable</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2157d6e6-0d60-45a2-9f5c-4096088cb2bb">Append</a>
</td>
<td align="left" width="63%">
Adds a file ID to a similarity file ID table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7c54c1a-0b02-43ae-975c-e94bd3dcac45">CloseTable</a>
</td>
<td align="left" width="63%">
Closes a similarity file ID table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc683c53-5491-4cc6-abe1-c82e69aaa7f4">CreateTable</a>
</td>
<td align="left" width="63%">
Creates or opens a similarity file ID table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e472ab0-efa4-4edd-8d78-68d5a66cf41c">CreateTableIndirect</a>
</td>
<td align="left" width="63%">
Creates or opens a similarity file ID table using the RDC application's implementation of the <a href="https://msdn.microsoft.com/8b6ac8d0-37fd-4bd3-aa44-5b57f546364d">IRdcFileWriter</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d95140e-c422-4aa5-aea2-ee777f977c17">GetRecordCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of records that are stored in a similarity file ID table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fdd6ff92-d312-4789-b535-4859fa7c871c">Invalidate</a>
</td>
<td align="left" width="63%">
Marks a file ID as not valid in the similarity file ID table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf9dbeb1-0182-4927-80ad-bb51fab2e637">Lookup</a>
</td>
<td align="left" width="63%">
Retrieves the file ID in the similarity file ID table that corresponds to a given file index.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

