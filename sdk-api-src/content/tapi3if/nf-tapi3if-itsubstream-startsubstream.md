---
UID: NF:tapi3if.ITSubStream.StartSubStream
title: ITSubStream::StartSubStream
author: windows-sdk-content
description: The StartSubStream method starts the substream. See the Remarks section under ITStream::StartStream for additional information.
old-location: tapi3\itsubstream_startsubstream.htm
old-project: Tapi
ms.assetid: 603cb667-a108-4e47-9808-99fddad5d894
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITSubStream interface [TAPI 2.2],StartSubStream method, ITSubStream.StartSubStream, ITSubStream::StartSubStream, StartSubStream, StartSubStream method [TAPI 2.2], StartSubStream method [TAPI 2.2],ITSubStream interface, _tapi3_itsubstream_startsubstream, tapi3.itsubstream_startsubstream, tapi3if/ITSubStream::StartSubStream
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
 - ITSubStream.StartSubStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITSubStream::StartSubStream


## -description


The <b>StartSubStream</b> method starts the substream. See the Remarks section under 
<a href="https://msdn.microsoft.com/23553f00-5ce5-465e-b455-8bf2d73dae9d">ITStream::StartStream</a> for additional information.


## -parameters






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
<dt><b>TAPI_E_NOTERMINALSELECTED</b></dt>
</dl>
</td>
<td width="60%">
No terminal has been selected on the substream so it cannot be started.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTSTOPPED</b></dt>
</dl>
</td>
<td width="60%">
Substream has already been started.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This operation is not supported.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

