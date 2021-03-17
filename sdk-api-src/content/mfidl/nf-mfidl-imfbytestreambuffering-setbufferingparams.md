---
UID: NF:mfidl.IMFByteStreamBuffering.SetBufferingParams
title: IMFByteStreamBuffering::SetBufferingParams (mfidl.h)
description: Sets the buffering parameters.
helpviewer_keywords: ["033ea7d4-d669-497b-be37-a8c9a6584209","IMFByteStreamBuffering interface [Media Foundation]","SetBufferingParams method","IMFByteStreamBuffering.SetBufferingParams","IMFByteStreamBuffering::SetBufferingParams","SetBufferingParams","SetBufferingParams method [Media Foundation]","SetBufferingParams method [Media Foundation]","IMFByteStreamBuffering interface","mf.imfbytestreambuffering_setbufferingparams","mfidl/IMFByteStreamBuffering::SetBufferingParams"]
old-location: mf\imfbytestreambuffering_setbufferingparams.htm
tech.root: mf
ms.assetid: 033ea7d4-d669-497b-be37-a8c9a6584209
ms.date: 12/05/2018
ms.keywords: 033ea7d4-d669-497b-be37-a8c9a6584209, IMFByteStreamBuffering interface [Media Foundation],SetBufferingParams method, IMFByteStreamBuffering.SetBufferingParams, IMFByteStreamBuffering::SetBufferingParams, SetBufferingParams, SetBufferingParams method [Media Foundation], SetBufferingParams method [Media Foundation],IMFByteStreamBuffering interface, mf.imfbytestreambuffering_setbufferingparams, mfidl/IMFByteStreamBuffering::SetBufferingParams
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
 - IMFByteStreamBuffering::SetBufferingParams
 - mfidl/IMFByteStreamBuffering::SetBufferingParams
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
 - IMFByteStreamBuffering.SetBufferingParams
---

# IMFByteStreamBuffering::SetBufferingParams


## -description

Sets the buffering parameters.

## -parameters

### -param pParams [in]

Pointer to an <a href="/windows/desktop/api/mfidl/ns-mfidl-mfbytestream_buffering_params">MFBYTESTREAM_BUFFERING_PARAMS</a> structure that contains the buffering parameters. The byte stream uses this information to calculate how much data to buffer from the network.

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
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering">IMFByteStreamBuffering</a>