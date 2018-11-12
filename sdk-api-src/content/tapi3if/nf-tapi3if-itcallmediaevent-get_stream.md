---
UID: NF:tapi3if.ITCallMediaEvent.get_Stream
title: ITCallMediaEvent::get_Stream
author: windows-sdk-content
description: The get_Stream method gets a pointer to the ITStream interface associated with the call media event.
old-location: tapi3\itcallmediaevent_get_stream.htm
tech.root: tapi
ms.assetid: 2afcb8ee-1f8c-41d0-8a8f-f34ebf09d224
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITCallMediaEvent interface [TAPI 2.2],get_Stream method, ITCallMediaEvent.get_Stream, ITCallMediaEvent::get_Stream, _tapi3_itcallmediaevent_get_stream, get_Stream, get_Stream method [TAPI 2.2], get_Stream method [TAPI 2.2],ITCallMediaEvent interface, tapi3.itcallmediaevent_get_stream, tapi3if/ITCallMediaEvent::get_Stream
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCallMediaEvent.get_Stream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallMediaEvent::get_Stream


## -description


The 
<b>get_Stream</b> method gets a pointer to the 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface associated with the call media event.


## -parameters




### -param ppStream [out]

Pointer to 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface pointer.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppStream</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface returned by <b>ITCallMediaEvent::get_Stream</b>. The application must call <b>Release</b> on 
<b>ITStream</b> to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/db55ff03-9271-4a94-9cba-a3ef0282b7b6">ITCallMediaEvent</a>



<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>
 

 

