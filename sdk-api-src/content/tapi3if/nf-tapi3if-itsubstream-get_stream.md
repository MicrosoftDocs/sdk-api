---
UID: NF:tapi3if.ITSubStream.get_Stream
title: ITSubStream::get_Stream
author: windows-sdk-content
description: The get_Stream method retrieves the pointer to the ITStream interface for the current substream.
old-location: tapi3\itsubstream_get_stream.htm
old-project: Tapi
ms.assetid: ec97e621-3789-46a4-b6b6-96639c5e7d4f
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITSubStream interface [TAPI 2.2],get_Stream method, ITSubStream.get_Stream, ITSubStream::get_Stream, _tapi3_itsubstream_get_stream, get_Stream, get_Stream method [TAPI 2.2], get_Stream method [TAPI 2.2],ITSubStream interface, tapi3.itsubstream_get_stream, tapi3if/ITSubStream::get_Stream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tapi3if.h
api_name:
-	ITSubStream.get_Stream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITSubStream::get_Stream


## -description


The 
<b>get_Stream</b> method retrieves the pointer to the 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface for the current substream.


## -parameters




### -param ppITStream [out]

Pointer to current 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface.


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
The <i>ppITStream</i> parameter is not a valid pointer.

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
</table>
 




## -remarks



TAPI calls the <a href="_com_iunknown_addref">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface returned by <b>ITSubStream::get_Stream</b>. The application must call <a href="_com_iunknown_release">Release</a> on the 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

