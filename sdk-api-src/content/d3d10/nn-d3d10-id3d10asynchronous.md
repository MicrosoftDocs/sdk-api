---
UID: NN:d3d10.ID3D10Asynchronous
title: ID3D10Asynchronous
author: windows-sdk-content
description: This interface encapsulates methods for retrieving data from the GPU asynchronously.
old-location: direct3d10\id3d10asynchronous.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10asynchronous.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: ID3D10Asynchronous, ID3D10Asynchronous interface [Direct3D 10], ID3D10Asynchronous interface [Direct3D 10],described, bbcae8e9-6f10-e6ca-52e5-20302edce780, d3d10/ID3D10Asynchronous, direct3d10.id3d10asynchronous
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d10.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D10_USAGE
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Asynchronous interface


## -description


This interface encapsulates methods for retrieving data from the GPU asynchronously.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Asynchronous</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>. <b>ID3D10Asynchronous</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb173501(v=VS.85).aspx">Begin</a>
</td>
<td align="left" width="63%">
Starts the collection of GPU data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173502(v=VS.85).aspx">End</a>
</td>
<td align="left" width="63%">
Ends the collection of GPU data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173503(v=VS.85).aspx">GetData</a>
</td>
<td align="left" width="63%">
Get data from the GPU asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb173504(v=VS.85).aspx">GetDataSize</a>
</td>
<td align="left" width="63%">
Get the size of the data (in bytes) that is output when calling <a href="https://msdn.microsoft.com/en-us/library/Bb173503(v=VS.85).aspx">ID3D10Asynchronous::GetData</a>.

</td>
</tr>
</table> 


## -remarks



There are three types of asynchronous interfaces, all of which inherit this interface:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173823(v=VS.85).aspx">ID3D10Query Interface</a> - Queries information from the GPU.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173822(v=VS.85).aspx">ID3D10Predicate Interface</a> - Determines whether a piece of geometry should be processed or not depending on the results of a previous draw call.</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Bb173514(v=VS.85).aspx">ID3D10Counter Interface</a> - Measures GPU performance.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205152(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173529(v=VS.85).aspx">ID3D10DeviceChild</a>
 

 

