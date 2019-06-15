---
UID: NN:d3d10.ID3D10Asynchronous
title: ID3D10Asynchronous (d3d10.h)
author: windows-sdk-content
description: This interface encapsulates methods for retrieving data from the GPU asynchronously.
old-location: direct3d10\id3d10asynchronous.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10asynchronous.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D10Asynchronous, ID3D10Asynchronous interface [Direct3D 10], ID3D10Asynchronous interface [Direct3D 10],described, bbcae8e9-6f10-e6ca-52e5-20302edce780, d3d10/ID3D10Asynchronous, direct3d10.id3d10asynchronous
ms.topic: interface
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Asynchronous
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Asynchronous interface


## -description


This interface encapsulates methods for retrieving data from the GPU asynchronously.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Asynchronous</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>. <b>ID3D10Asynchronous</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Asynchronous</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-begin">Begin</a>
</td>
<td align="left" width="63%">
Starts the collection of GPU data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-end">End</a>
</td>
<td align="left" width="63%">
Ends the collection of GPU data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">GetData</a>
</td>
<td align="left" width="63%">
Get data from the GPU asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdatasize">GetDataSize</a>
</td>
<td align="left" width="63%">
Get the size of the data (in bytes) that is output when calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">ID3D10Asynchronous::GetData</a>.

</td>
</tr>
</table> 


## -remarks



There are three types of asynchronous interfaces, all of which inherit this interface:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10query">ID3D10Query Interface</a> - Queries information from the GPU.</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10predicate">ID3D10Predicate Interface</a> - Determines whether a piece of geometry should be processed or not depending on the results of a previous draw call.</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10counter">ID3D10Counter Interface</a> - Measures GPU performance.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10devicechild">ID3D10DeviceChild</a>
 

 

