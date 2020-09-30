---
UID: NF:mfidl.IMFSensorStream.CloneSensorStream
title: IMFSensorStream::CloneSensorStream (mfidl.h)
description: Clones the IMFSensorStream.
helpviewer_keywords: ["CloneSensorStream","CloneSensorStream method [Media Foundation]","CloneSensorStream method [Media Foundation]","IMFSensorStream interface","IMFSensorStream interface [Media Foundation]","CloneSensorStream method","IMFSensorStream.CloneSensorStream","IMFSensorStream::CloneSensorStream","mf.imfsensorstream_clonesensorstream","mfidl/IMFSensorStream::CloneSensorStream"]
old-location: mf\imfsensorstream_clonesensorstream.htm
tech.root: mf
ms.assetid: A9729DEB-AA59-476B-A309-A960C3B1E40E
ms.date: 12/05/2018
ms.keywords: CloneSensorStream, CloneSensorStream method [Media Foundation], CloneSensorStream method [Media Foundation],IMFSensorStream interface, IMFSensorStream interface [Media Foundation],CloneSensorStream method, IMFSensorStream.CloneSensorStream, IMFSensorStream::CloneSensorStream, mf.imfsensorstream_clonesensorstream, mfidl/IMFSensorStream::CloneSensorStream
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorStream::CloneSensorStream
 - mfidl/IMFSensorStream::CloneSensorStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorStream.CloneSensorStream
---

# IMFSensorStream::CloneSensorStream


## -description

Clones the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorstream">IMFSensorStream</a>.

## -parameters

### -param ppStream [out]

If the call is successful, <i>ppStream</i> receives the cloned <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorstream">IMFSensorStream</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppStream</i> parameter is null.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorstream">IMFSensorStream</a>