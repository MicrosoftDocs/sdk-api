---
UID: NF:sbe.IStreamBufferConfigure2.SetMultiplexedPacketSize
title: IStreamBufferConfigure2::SetMultiplexedPacketSize (sbe.h)
description: The SetMultiplexedPacketSize method sets the size of the multiplexed packets in the backing files for the Stream Buffer Engine.
helpviewer_keywords: ["IStreamBufferConfigure2 interface [Microsoft TV Technologies]","SetMultiplexedPacketSize method","IStreamBufferConfigure2.SetMultiplexedPacketSize","IStreamBufferConfigure2::SetMultiplexedPacketSize","IStreamBufferConfigure2SetMultiplexedPacketSize","SetMultiplexedPacketSize","SetMultiplexedPacketSize method [Microsoft TV Technologies]","SetMultiplexedPacketSize method [Microsoft TV Technologies]","IStreamBufferConfigure2 interface","mstv.istreambufferconfigure2_setmultiplexedpacketsize","sbe/IStreamBufferConfigure2::SetMultiplexedPacketSize"]
old-location: mstv\istreambufferconfigure2_setmultiplexedpacketsize.htm
tech.root: mstv
ms.assetid: 9133331b-cf0c-4dfb-8bb6-101742d194c7
ms.date: 12/05/2018
ms.keywords: IStreamBufferConfigure2 interface [Microsoft TV Technologies],SetMultiplexedPacketSize method, IStreamBufferConfigure2.SetMultiplexedPacketSize, IStreamBufferConfigure2::SetMultiplexedPacketSize, IStreamBufferConfigure2SetMultiplexedPacketSize, SetMultiplexedPacketSize, SetMultiplexedPacketSize method [Microsoft TV Technologies], SetMultiplexedPacketSize method [Microsoft TV Technologies],IStreamBufferConfigure2 interface, mstv.istreambufferconfigure2_setmultiplexedpacketsize, sbe/IStreamBufferConfigure2::SetMultiplexedPacketSize
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
 - IStreamBufferConfigure2::SetMultiplexedPacketSize
 - sbe/IStreamBufferConfigure2::SetMultiplexedPacketSize
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
 - IStreamBufferConfigure2.SetMultiplexedPacketSize
---

# IStreamBufferConfigure2::SetMultiplexedPacketSize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SetMultiplexedPacketSize</b> method sets the size of the multiplexed packets in the backing files for the Stream Buffer Engine.

## -parameters

### -param cbBytesPerPacket [in]

Specifies the packet size, in bytes. The value must be between 8192 and 65535, inclusive. The default value is 65535.

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

For low-bit-rate streams, the default packet size may be unnecessarily large. You can use this method to reduce the packet size.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferconfigure2">IStreamBufferConfigure2 Interface</a>