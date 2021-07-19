---
UID: NF:mfidl.IMFByteStreamBuffering.StopBuffering
title: IMFByteStreamBuffering::StopBuffering (mfidl.h)
description: Stops any buffering that is in progress.
helpviewer_keywords: ["IMFByteStreamBuffering interface [Media Foundation]","StopBuffering method","IMFByteStreamBuffering.StopBuffering","IMFByteStreamBuffering::StopBuffering","StopBuffering","StopBuffering method [Media Foundation]","StopBuffering method [Media Foundation]","IMFByteStreamBuffering interface","da342ac4-bb61-40d6-9b67-0480ac2a780f","mf.imfbytestreambuffering_stopbuffering","mfidl/IMFByteStreamBuffering::StopBuffering"]
old-location: mf\imfbytestreambuffering_stopbuffering.htm
tech.root: mf
ms.assetid: da342ac4-bb61-40d6-9b67-0480ac2a780f
ms.date: 12/05/2018
ms.keywords: IMFByteStreamBuffering interface [Media Foundation],StopBuffering method, IMFByteStreamBuffering.StopBuffering, IMFByteStreamBuffering::StopBuffering, StopBuffering, StopBuffering method [Media Foundation], StopBuffering method [Media Foundation],IMFByteStreamBuffering interface, da342ac4-bb61-40d6-9b67-0480ac2a780f, mf.imfbytestreambuffering_stopbuffering, mfidl/IMFByteStreamBuffering::StopBuffering
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFByteStreamBuffering::StopBuffering
 - mfidl/IMFByteStreamBuffering::StopBuffering
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFByteStreamBuffering.StopBuffering
---

# IMFByteStreamBuffering::StopBuffering


## -description

Stops any buffering that is in progress.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The byte stream successfully stopped buffering.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No buffering was in progress.

</td>
</tr>
</table>

## -remarks

If the byte stream is currently buffering data, it stops and sends an <a href="/windows/desktop/medfound/mebufferingstopped">MEBufferingStopped</a> event. If the byte stream is not currently buffering, this method has no effect.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering">IMFByteStreamBuffering</a>
