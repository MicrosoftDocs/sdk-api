---
UID: NF:sbe.IStreamBufferConfigure2.GetMultiplexedPacketSize
title: IStreamBufferConfigure2::GetMultiplexedPacketSize (sbe.h)
description: The GetMultiplexedPacketSize method returns the size of the multiplexed packets in the backing files for the Stream Buffer Engine.
helpviewer_keywords: ["GetMultiplexedPacketSize","GetMultiplexedPacketSize method [Microsoft TV Technologies]","GetMultiplexedPacketSize method [Microsoft TV Technologies]","IStreamBufferConfigure2 interface","IStreamBufferConfigure2 interface [Microsoft TV Technologies]","GetMultiplexedPacketSize method","IStreamBufferConfigure2.GetMultiplexedPacketSize","IStreamBufferConfigure2::GetMultiplexedPacketSize","IStreamBufferConfigure2GetMultiplexedPacketSize","mstv.istreambufferconfigure2_getmultiplexedpacketsize","sbe/IStreamBufferConfigure2::GetMultiplexedPacketSize"]
old-location: mstv\istreambufferconfigure2_getmultiplexedpacketsize.htm
tech.root: mstv
ms.assetid: 36b5cd06-ba6a-4546-98b6-4c8b47f7f62b
ms.date: 12/05/2018
ms.keywords: GetMultiplexedPacketSize, GetMultiplexedPacketSize method [Microsoft TV Technologies], GetMultiplexedPacketSize method [Microsoft TV Technologies],IStreamBufferConfigure2 interface, IStreamBufferConfigure2 interface [Microsoft TV Technologies],GetMultiplexedPacketSize method, IStreamBufferConfigure2.GetMultiplexedPacketSize, IStreamBufferConfigure2::GetMultiplexedPacketSize, IStreamBufferConfigure2GetMultiplexedPacketSize, mstv.istreambufferconfigure2_getmultiplexedpacketsize, sbe/IStreamBufferConfigure2::GetMultiplexedPacketSize
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamBufferConfigure2::GetMultiplexedPacketSize
 - sbe/IStreamBufferConfigure2::GetMultiplexedPacketSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferConfigure2.GetMultiplexedPacketSize
---

# IStreamBufferConfigure2::GetMultiplexedPacketSize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetMultiplexedPacketSize</b> method returns the size of the multiplexed packets in the backing files for the Stream Buffer Engine.

## -parameters

### -param pcbBytesPerPacket [out]

Receives the packet size, in bytes.

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

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure2">IStreamBufferConfigure2 Interface</a>