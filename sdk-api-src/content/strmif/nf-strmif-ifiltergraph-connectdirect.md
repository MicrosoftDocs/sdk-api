---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IFilterGraph::ConnectDirect


## -description



The <code>ConnectDirect</code> method connects the two pins directly (without intervening filters).




## -parameters




### -param ppinOut [in]

Pointer to the output pin.


### -param ppinIn [in]

Pointer to the input pin.


### -param pmt [in]

Pointer to the media type to use for the connection (optional; can be <b>NULL</b>).


## -returns



Returns one of the following values, or an error value returned by <a href="https://msdn.microsoft.com/1b02ee67-5dc5-44c1-bea5-2eab46ebd0f6">IPin::Connect</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_IN_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
One of the specified pins is not in the graph.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_CIRCULAR_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The input pin is upstream of the output pin, which would result in a circular graph.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph Interface</a>
 

 

