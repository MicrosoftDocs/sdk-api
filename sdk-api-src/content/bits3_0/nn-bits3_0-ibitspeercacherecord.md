---
UID: NN:bits3_0.IBitsPeerCacheRecord
title: IBitsPeerCacheRecord
author: windows-sdk-content
description: Use IBitsPeerCacheRecord to get information about a file in the cache.
old-location: bits\ibitspeercacherecord.htm
tech.root: bits
ms.assetid: 61db33de-a38c-4c52-9f1b-66d46f25c297
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBitsPeerCacheRecord, IBitsPeerCacheRecord interface [BITS], IBitsPeerCacheRecord interface [BITS],described, bits.ibitspeercacherecord, bits3_0/IBitsPeerCacheRecord
ms.prod: windows-hardware
ms.technology: windows-devices
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
<a href="https://msdn.microsoft.com/en-us/library/Aa964287(v=VS.85).aspx">IBitsPeerCacheAdministration::GetRecord</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa964305(v=VS.85).aspx">IEnumBitsPeerCacheRecords::Next</a>
</li>
</ul>

<div class="alert"><b>Note</b>  This interface is deprecated in BITS 4.0, and all of the API methods will return <b>S_FALSE</b>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBitsPeerCacheRecord</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IBitsPeerCacheRecord</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa964292(v=VS.85).aspx">GetFileModificationTime</a>
</td>
<td align="left" width="63%">
Gets the date and time that the file was last modified on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964293(v=VS.85).aspx">GetFileRanges</a>
</td>
<td align="left" width="63%">
Gets the ranges of the file that are in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964294(v=VS.85).aspx">GetFileSize</a>
</td>
<td align="left" width="63%">
Gets the size of the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964295(v=VS.85).aspx">GetId</a>
</td>
<td align="left" width="63%">
Get the identifier that uniquely identifies the record in the cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964296(v=VS.85).aspx">GetLastAccessTime</a>
</td>
<td align="left" width="63%">
Get the date and time that the file was last accessed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964297(v=VS.85).aspx">GetOriginUrl</a>
</td>
<td align="left" width="63%">
Gets the origin URL of the cached file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa964298(v=VS.85).aspx">IsFileValidated</a>
</td>
<td align="left" width="63%">
Determines whether the file has been validated.

</td>
</tr>
</table> 

