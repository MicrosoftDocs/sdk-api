---
UID: NN:d3d9helper.IDirect3DQuery9
title: IDirect3DQuery9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DQuery9 interface to perform asynchronous queries on a driver.
old-location: direct3d9\idirect3dquery9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dquery9.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 6e601b3e-6b1d-4777-8fd2-a1c3ed1d5565, IDirect3DQuery9, IDirect3DQuery9 interface [Direct3D 9], IDirect3DQuery9 interface [Direct3D 9],described, d3d9helper/IDirect3DQuery9, direct3d9.idirect3dquery9
ms.topic: interface
req.header: d3d9helper.h
req.include-header: D3D9.h
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
req.lib: D3d9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.lib
 - d3d9.dll
api_name:
 - IDirect3DQuery9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DQuery9 interface


## -description


Applications use the methods of the IDirect3DQuery9 interface to perform asynchronous queries on a driver.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DQuery9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirect3DQuery9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DQuery9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205873(v=VS.85).aspx">GetData</a>
</td>
<td align="left" width="63%">
Polls a queried resource to get the query state or a query result. For more information about queries, see <a href="https://msdn.microsoft.com/en-us/library/Bb147308(v=VS.85).aspx">Queries (Direct3D 9)</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205874(v=VS.85).aspx">GetDataSize</a>
</td>
<td align="left" width="63%">
Gets the number of bytes in the query data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205875(v=VS.85).aspx">GetDevice</a>
</td>
<td align="left" width="63%">
Gets the device that is being queried.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205876(v=VS.85).aspx">GetType</a>
</td>
<td align="left" width="63%">
Gets the query type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205877(v=VS.85).aspx">Issue</a>
</td>
<td align="left" width="63%">
Issue a query.

</td>
</tr>
</table> 


## -remarks



The LPDIRECT3DQUERY9 and PDIRECT3DQUERY9 types are defined as pointers to the <b>IDirect3DQuery9</b> interface.
    
            

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef struct IDirect3DQuery9 *LPDIRECT3DQUERY9, *PDIRECT3DQUERY9;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>
 

 

