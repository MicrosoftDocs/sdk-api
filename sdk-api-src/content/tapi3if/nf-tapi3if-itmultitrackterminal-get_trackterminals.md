---
UID: NF:tapi3if.ITMultiTrackTerminal.get_TrackTerminals
title: ITMultiTrackTerminal::get_TrackTerminals
author: windows-sdk-content
description: The get_TrackTerminals method creates and returns a collection containing the terminals contained by the multitrack terminal on which this method was called.
old-location: tapi3\itmultitrackterminal_get_trackterminals.htm
old-project: tapi
ms.assetid: 2bedefe8-6b84-48c0-8a7b-719d017baf24
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITMultiTrackTerminal interface [TAPI 2.2],get_TrackTerminals method, ITMultiTrackTerminal.get_TrackTerminals, ITMultiTrackTerminal::get_TrackTerminals, _tapi3_itmultitrackterminal_get_trackterminals, get_TrackTerminals, get_TrackTerminals method [TAPI 2.2], get_TrackTerminals method [TAPI 2.2],ITMultiTrackTerminal interface, tapi3.itmultitrackterminal_get_trackterminals, tapi3if/ITMultiTrackTerminal::get_TrackTerminals
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMultiTrackTerminal.get_TrackTerminals
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITMultiTrackTerminal::get_TrackTerminals


## -description


The 
<b>get_TrackTerminals</b> method creates and returns a collection containing the terminals contained by the multitrack terminal on which this method was called. The variant returned contains a pointer to an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> interface that can be used to iterate through elements of type 
<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>. The elements of the collection contain pointers to tracks.


## -parameters




### -param pVariant [out]

Pointer to a VARIANT containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface pointers for the tracks available.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter was not empty.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface returned by <b>ITMultiTrackTerminal::get_TrackTerminals</b>. The application must call <b>Release</b> on the 
<b>ITTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>



<a href="https://msdn.microsoft.com/c9e5d8a4-78a6-4449-9c11-c780e72ab925">ITMultiTrackTerminal</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>
 

 

