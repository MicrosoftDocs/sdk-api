---
UID: NN:structuredquerycondition.IRichChunk
title: IRichChunk (structuredquerycondition.h)
author: windows-sdk-content
description: Represents a chunk of data as a string and a PROPVARIANT value.
old-location: search\_search_IRichChunk.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irichchunk\irichchunk.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRichChunk, IRichChunk interface [search], IRichChunk interface [search],described, _search_IRichChunk, search._search_IRichChunk, structuredquerycondition/IRichChunk
ms.topic: interface
f1_keywords: 
 - "structuredquerycondition/IRichChunk"
req.header: structuredquerycondition.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structureduuerycondition.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquerycondition.h
api_name:
 - IRichChunk
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IRichChunk interface


## -description


Represents a chunk of data as a string and a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> value.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRichChunk</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRichChunk</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRichChunk</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-irichchunk-getdata">GetData</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> and input string that represents a chunk of data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/search/irichchunk-remotegetdata">RemoteGetData</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> and input string that represents a chunk of data.

</td>
</tr>
</table> 


## -remarks



In Windows 7, this interface is defined in structuredquerycondition.idl and structuredquerycondition.h. Prior to Windows 7 this interface was declared in structuredquery.h and structuredquery.idl.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iquerysolution-geterrors">GetErrors</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/ne-structuredquery-tagstructured_query_parse_error">STRUCTURED_QUERY_PARSE_ERROR</a>
 

 

