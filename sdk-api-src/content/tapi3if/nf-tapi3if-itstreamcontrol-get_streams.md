---
UID: NF:tapi3if.ITStreamControl.get_Streams
title: ITStreamControl::get_Streams
author: windows-sdk-content
description: The get_Streams method creates a collection of media streams currently available on the call. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateStreams method.
old-location: tapi3\itstreamcontrol_get_streams.htm
old-project: tapi
ms.assetid: 4d001f5a-7731-47b9-8c68-e4dd2d0bf02f
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITStreamControl interface [TAPI 2.2],get_Streams method, ITStreamControl.get_Streams, ITStreamControl::get_Streams, _tapi3_itstreamcontrol_get_streams, get_Streams, get_Streams method [TAPI 2.2], get_Streams method [TAPI 2.2],ITStreamControl interface, tapi3.itstreamcontrol_get_streams, tapi3if/ITStreamControl::get_Streams
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITStreamControl.get_Streams
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITStreamControl::get_Streams


## -description


The 
<b>get_Streams</b> method creates a collection of media streams currently available on the call. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/de018f3e-d3b9-4093-a2b5-4929ac4d1d2a">EnumerateStreams</a> method.


## -parameters




### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface pointers.


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
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface returned by <b>ITStreamControl::get_Stream</b>. The application must call <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> on the 
<b>ITStream</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>



<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/12b9457a-7afb-4348-93a2-28728c673929">ITStreamControl</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

