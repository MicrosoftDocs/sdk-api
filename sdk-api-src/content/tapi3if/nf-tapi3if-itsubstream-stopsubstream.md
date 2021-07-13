---
UID: NF:tapi3if.ITSubStream.StopSubStream
title: ITSubStream::StopSubStream (tapi3if.h)
description: The StopSubStream method stops the substream. For additional information, see ITStream::StopStream.
helpviewer_keywords: ["ITSubStream interface [TAPI 2.2]","StopSubStream method","ITSubStream.StopSubStream","ITSubStream::StopSubStream","StopSubStream","StopSubStream method [TAPI 2.2]","StopSubStream method [TAPI 2.2]","ITSubStream interface","_tapi3_itsubstream_stopsubstream","tapi3.itsubstream_stopsubstream","tapi3if/ITSubStream::StopSubStream"]
old-location: tapi3\itsubstream_stopsubstream.htm
tech.root: tapi3
ms.assetid: fa5028f6-80eb-4076-a81c-c83b462fc27c
ms.date: 12/05/2018
ms.keywords: ITSubStream interface [TAPI 2.2],StopSubStream method, ITSubStream.StopSubStream, ITSubStream::StopSubStream, StopSubStream, StopSubStream method [TAPI 2.2], StopSubStream method [TAPI 2.2],ITSubStream interface, _tapi3_itsubstream_stopsubstream, tapi3.itsubstream_stopsubstream, tapi3if/ITSubStream::StopSubStream
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
 - ITSubStream::StopSubStream
 - tapi3if/ITSubStream::StopSubStream
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
 - ITSubStream.StopSubStream
---

# ITSubStream::StopSubStream


## -description

The 
<b>StopSubStream</b> method stops the substream. For additional information, see 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-stopstream">ITStream::StopStream</a>.



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
<dt><b>TAPI_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The provider does not support this operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
