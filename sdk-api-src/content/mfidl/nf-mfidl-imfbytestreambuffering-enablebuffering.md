---
UID: NF:mfidl.IMFByteStreamBuffering.EnableBuffering
title: IMFByteStreamBuffering::EnableBuffering (mfidl.h)
description: Enables or disables buffering.
helpviewer_keywords: ["5f7418ff-32e5-49b3-b7b3-6686e6562d51","EnableBuffering","EnableBuffering method [Media Foundation]","EnableBuffering method [Media Foundation]","IMFByteStreamBuffering interface","IMFByteStreamBuffering interface [Media Foundation]","EnableBuffering method","IMFByteStreamBuffering.EnableBuffering","IMFByteStreamBuffering::EnableBuffering","mf.imfbytestreambuffering_enablebuffering","mfidl/IMFByteStreamBuffering::EnableBuffering"]
old-location: mf\imfbytestreambuffering_enablebuffering.htm
tech.root: mf
ms.assetid: 5f7418ff-32e5-49b3-b7b3-6686e6562d51
ms.date: 12/05/2018
ms.keywords: 5f7418ff-32e5-49b3-b7b3-6686e6562d51, EnableBuffering, EnableBuffering method [Media Foundation], EnableBuffering method [Media Foundation],IMFByteStreamBuffering interface, IMFByteStreamBuffering interface [Media Foundation],EnableBuffering method, IMFByteStreamBuffering.EnableBuffering, IMFByteStreamBuffering::EnableBuffering, mf.imfbytestreambuffering_enablebuffering, mfidl/IMFByteStreamBuffering::EnableBuffering
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
 - IMFByteStreamBuffering::EnableBuffering
 - mfidl/IMFByteStreamBuffering::EnableBuffering
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
 - IMFByteStreamBuffering.EnableBuffering
---

# IMFByteStreamBuffering::EnableBuffering


## -description

Enables or disables buffering.

## -parameters

### -param fEnable [in]

Specifies whether the byte stream buffers data. If <b>TRUE</b>, buffering is enabled. If <b>FALSE</b>, buffering is disabled.

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

## -remarks

Before calling this method, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfbytestreambuffering-setbufferingparams">IMFByteStreamBuffering::SetBufferingParams</a> to set the buffering parameters on the byte stream.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering">IMFByteStreamBuffering</a>