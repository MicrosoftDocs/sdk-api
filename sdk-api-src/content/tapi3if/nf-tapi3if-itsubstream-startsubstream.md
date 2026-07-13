---
UID: NF:tapi3if.ITSubStream.StartSubStream
title: ITSubStream::StartSubStream (tapi3if.h)
description: The StartSubStream method starts the substream. See the Remarks section under ITStream::StartStream for additional information.
helpviewer_keywords: ["ITSubStream interface [TAPI 2.2]","StartSubStream method","ITSubStream.StartSubStream","ITSubStream::StartSubStream","StartSubStream","StartSubStream method [TAPI 2.2]","StartSubStream method [TAPI 2.2]","ITSubStream interface","_tapi3_itsubstream_startsubstream","tapi3.itsubstream_startsubstream","tapi3if/ITSubStream::StartSubStream"]
old-location: tapi3\itsubstream_startsubstream.htm
tech.root: tapi3
ms.assetid: 603cb667-a108-4e47-9808-99fddad5d894
ms.date: 12/05/2018
ms.keywords: ITSubStream interface [TAPI 2.2],StartSubStream method, ITSubStream.StartSubStream, ITSubStream::StartSubStream, StartSubStream, StartSubStream method [TAPI 2.2], StartSubStream method [TAPI 2.2],ITSubStream interface, _tapi3_itsubstream_startsubstream, tapi3.itsubstream_startsubstream, tapi3if/ITSubStream::StartSubStream
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITSubStream::StartSubStream
 - tapi3if/ITSubStream::StartSubStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITSubStream.StartSubStream
---

# ITSubStream::StartSubStream


## -description

The <b>StartSubStream</b> method starts the substream. See the Remarks section under 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-startstream">ITStream::StartStream</a> for additional information.



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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
