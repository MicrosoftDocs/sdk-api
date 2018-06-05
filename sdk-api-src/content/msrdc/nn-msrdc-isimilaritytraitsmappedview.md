---
UID: NN:msrdc.ISimilarityTraitsMappedView
title: ISimilarityTraitsMappedView
author: windows-sdk-content
description: Provides methods that an RDC application can implement for manipulating a mapped view of a similarity traits table file.
old-location: rdc\isimilaritytraitsmappedview.htm
old-project: Rdc
ms.assetid: 48d6d4a0-fbf1-476a-b30f-83176c51cb48
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ISimilarityTraitsMappedView, ISimilarityTraitsMappedView interface [Remote Differential Compression], ISimilarityTraitsMappedView interface [Remote Differential Compression],described, fs.isimilaritytraitsmappedview, msrdc/ISimilarityTraitsMappedView, rdc.isimilaritytraitsmappedview
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RdcMappingAccessMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsRdc.dll
api_name:
-	ISimilarityTraitsMappedView
product: Windows
targetos: Windows
req.lib: 
req.dll: MsRdc.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ISimilarityTraitsMappedView interface


## -description


Provides methods that an RDC application can implement for manipulating a mapped view of a similarity traits table file.

This interface is used together with the <a href="https://msdn.microsoft.com/1ddc599b-5a9b-4807-9005-00793f9a6ed4">ISimilarityTraitsMapping</a> interface to allow the application to provide the I/O services needed by the <a href="https://msdn.microsoft.com/0985e27c-aa70-43c1-bcec-00ef14f2df58">ISimilarityTraitsTable</a> and <a href="https://msdn.microsoft.com/fe0cd874-a40c-4d82-99bf-b84008a4995c">ISimilarity</a> interfaces. The implementation model is based on memory mapped files, but the interface is rich enough to support other models as well, such as memory-only arrays or traditional file accesses.

A mapped view is used to map an area of the entire file into a contiguous block of memory. This mapping is valid until the view is changed or unmapped. A possible implementation would call the <a href="https://msdn.microsoft.com/4ad4580d-c002-44a4-a5f6-757e83ed8732">ReadFile</a> function when the view is mapped (see the <a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a> method), and would then write the changes back to disk when the view is changed (see <b>Get</b>) or released (see the <a href="https://msdn.microsoft.com/37739164-eefd-4336-99bc-2074c8f2f294">Unmap</a> method).

There can be multiple overlapping read-only mapped views of the same area of a file, and one or more read-only views can overlap a read/write view, but there can be only one read/write view of a given area of a file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISimilarityTraitsMappedView</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISimilarityTraitsMappedView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISimilarityTraitsMappedView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh463886">Flush</a>
</td>
<td align="left" width="63%">
Writes to the disk any dirty pages within a mapped view of a similarity traits table file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>
</td>
<td align="left" width="63%">
Returns information about the mapped view of a similarity traits table file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac229f59-eb2f-471e-9f31-0e7139becdcb">GetView</a>
</td>
<td align="left" width="63%">
Returns the beginning and ending addresses for the mapped view of a similarity traits table file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37739164-eefd-4336-99bc-2074c8f2f294">Unmap</a>
</td>
<td align="left" width="63%">
Un-maps a mapped view of a similarity traits table file.

</td>
</tr>
</table> 

