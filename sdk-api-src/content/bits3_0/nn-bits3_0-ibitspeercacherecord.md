---
UID: NN:bits3_0.IBitsPeerCacheRecord
title: IBitsPeerCacheRecord (bits3_0.h)
author: windows-sdk-content
description: Use IBitsPeerCacheRecord to get information about a file in the cache.
old-location: bits\ibitspeercacherecord.htm
tech.root: Bits
ms.assetid: 61db33de-a38c-4c52-9f1b-66d46f25c297
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBitsPeerCacheRecord, IBitsPeerCacheRecord interface [BITS], IBitsPeerCacheRecord interface [BITS],described, bits.ibitspeercacherecord, bits3_0/IBitsPeerCacheRecord
ms.topic: interface
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBitsPeerCacheRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBitsPeerCacheRecord interface


## -description


Use <b>IBitsPeerCacheRecord</b> to get information about a file in the cache. 

To get this interface, call one of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/7dd32e9c-bf4e-4dbf-aa9f-9ffbf98d3f1c">IBitsPeerCacheAdministration::GetRecord</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a8117baa-9f77-4735-bd15-2c7e1e759e9b">IEnumBitsPeerCacheRecords::Next</a>
</li>
</ul>

<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBitsPeerCacheRecord</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBitsPeerCacheRecord</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBitsPeerCacheRecord</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe24b090-7dfd-4cbe-bb5d-ff3fd01723df">GetFileModificationTime</a>
</td>
<td align="left" width="63%">
Gets the date and time that the file was last modified on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63f9821c-f5b6-4646-96e0-4ec61ce16e9b">GetFileRanges</a>
</td>
<td align="left" width="63%">
Gets the ranges of the file that are in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b997cd0-a947-4ce7-b047-85268ea46b70">GetFileSize</a>
</td>
<td align="left" width="63%">
Gets the size of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1894ab3-0b3f-492b-8ed7-51f3b4ee1eaa">GetId</a>
</td>
<td align="left" width="63%">
Get the identifier that uniquely identifies the record in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4443db2-3d4f-497f-b2e3-d969d8271d6f">GetLastAccessTime</a>
</td>
<td align="left" width="63%">
Get the date and time that the file was last accessed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d74df3a-89e0-4a3a-82f3-c2e79c609b21">GetOriginUrl</a>
</td>
<td align="left" width="63%">
Gets the origin URL of the cached file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f492f009-bef7-412e-8626-ae84cd5ce03f">IsFileValidated</a>
</td>
<td align="left" width="63%">
Determines whether the file has been validated.

</td>
</tr>
</table> 

