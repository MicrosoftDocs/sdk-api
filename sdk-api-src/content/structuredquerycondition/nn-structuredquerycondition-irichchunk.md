---
UID: NN:structuredquerycondition.IRichChunk
title: IRichChunk
author: windows-sdk-content
description: Represents a chunk of data as a string and a PROPVARIANT value.
old-location: search\_search_IRichChunk.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irichchunk\irichchunk.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRichChunk, IRichChunk interface [search], IRichChunk interface [search],described, _search_IRichChunk, search._search_IRichChunk, structuredquerycondition/IRichChunk
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# IRichChunk interface


## -description


Represents a chunk of data as a string and a <a href="_stg_propvariant">PROPVARIANT</a> value.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRichChunk</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRichChunk</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/09a1a0f5-2779-4aa3-ba56-605e846de16d">GetData</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="_stg_propvariant">PROPVARIANT</a> and input string that represents a chunk of data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78846D1D-923F-4FEA-8BF2-B16BB1B21BB3">RemoteGetData</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="_stg_propvariant">PROPVARIANT</a> and input string that represents a chunk of data.

</td>
</tr>
</table> 


## -remarks



In Windows 7, this interface is defined in structuredquerycondition.idl and structuredquerycondition.h. Prior to Windows 7 this interface was declared in structuredquery.h and structuredquery.idl.




## -see-also




<a href="https://msdn.microsoft.com/50eead1a-5eb9-4bc9-ba54-c6dc77284f4d">GetErrors</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/abc76a8c-ee72-469a-85a0-75c12ee4e5d9">STRUCTURED_QUERY_PARSE_ERROR</a>
 

 

