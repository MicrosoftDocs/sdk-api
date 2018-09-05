---
UID: NN:msrdc.ISimilarityTraitsMapping
title: ISimilarityTraitsMapping
author: windows-sdk-content
description: Provides methods that an RDC application can implement for creating and manipulating a file mapping object for a similarity traits table file.
old-location: rdc\isimilaritytraitsmapping.htm
old-project: Rdc
ms.assetid: 1ddc599b-5a9b-4807-9005-00793f9a6ed4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISimilarityTraitsMapping, ISimilarityTraitsMapping interface [Remote Differential Compression], ISimilarityTraitsMapping interface [Remote Differential Compression],described, fs.isimilaritytraitsmapping, msrdc/ISimilarityTraitsMapping, rdc.isimilaritytraitsmapping
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
 - ISimilarityTraitsMapping
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarityTraitsMapping interface


## -description


Provides methods that an RDC application can implement for creating and manipulating a file mapping object for  a similarity traits table file.

This interface is used together with the <a href="https://msdn.microsoft.com/48d6d4a0-fbf1-476a-b30f-83176c51cb48">ISimilarityTraitsMappedView</a> interface to allow the application to provide the I/O services needed by the <a href="https://msdn.microsoft.com/0985e27c-aa70-43c1-bcec-00ef14f2df58">ISimilarityTraitsTable</a> and <a href="https://msdn.microsoft.com/fe0cd874-a40c-4d82-99bf-b84008a4995c">ISimilarity</a> interfaces. The implementation model is based on memory mapped files, but the interface is rich enough to support other models as well, such as memory-only arrays or traditional file accesses.

This interface is used to represent the file on which multiple read-only or read/write views can be created. There can be multiple overlapping read-only mapped views of the same area of a file, and one or more read-only views can overlap a read/write view, but there can be only one read/write view of a given area of a file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimilarityTraitsMapping</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISimilarityTraitsMapping</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISimilarityTraitsMapping</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ac20c6b-9fe5-4b59-a9ed-faef97fd76f2">CloseMapping</a>
</td>
<td align="left" width="63%">
Closes a file mapping object for a similarity traits table file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/222b3682-8ccc-4c52-858a-ad4ac8a65add">CreateView</a>
</td>
<td align="left" width="63%">
Maps a view of the file mapping for a similarity traits table file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/920b9c77-ca45-42ff-801f-cbe1ab3eab2c">GetFileSize</a>
</td>
<td align="left" width="63%">
Returns the size of a similarity traits table file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8189d346-9e8e-40c0-8080-75c36326c917">GetPageSize</a>
</td>
<td align="left" width="63%">
Returns the page size (disk block size) for a similarity traits table file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/278d7b78-28c6-41ee-9060-5f7d757ef494">OpenMapping</a>
</td>
<td align="left" width="63%">
Opens the file mapping object for a similarity traits table file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea4fe3f9-7422-4673-90e4-4907fb8dd690">ResizeMapping</a>
</td>
<td align="left" width="63%">
Resizes the file mapping object for a similarity traits table file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f8afa56-6531-40dd-979f-12506ad8c286">SetFileSize</a>
</td>
<td align="left" width="63%">
Sets the size of a similarity traits table file.

</td>
</tr>
</table> 

