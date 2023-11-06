---
UID: NF:mpeg2data.IMpeg2Stream.SupplyDataBuffer
title: IMpeg2Stream::SupplyDataBuffer (mpeg2data.h)
description: The SupplyDataBuffer method provides a buffer for the Mpeg2Stream object to write data.
helpviewer_keywords: ["IMpeg2Stream interface [Microsoft TV Technologies]","SupplyDataBuffer method","IMpeg2Stream.SupplyDataBuffer","IMpeg2Stream::SupplyDataBuffer","IMpeg2StreamSupplyDataBuffer","SupplyDataBuffer","SupplyDataBuffer method [Microsoft TV Technologies]","SupplyDataBuffer method [Microsoft TV Technologies]","IMpeg2Stream interface","mpeg2data/IMpeg2Stream::SupplyDataBuffer","mstv.impeg2stream_supplydatabuffer"]
old-location: mstv\impeg2stream_supplydatabuffer.htm
tech.root: mstv
ms.assetid: 68950eba-6c23-49f7-9651-d4db9e554de3
ms.date: 12/05/2018
ms.keywords: IMpeg2Stream interface [Microsoft TV Technologies],SupplyDataBuffer method, IMpeg2Stream.SupplyDataBuffer, IMpeg2Stream::SupplyDataBuffer, IMpeg2StreamSupplyDataBuffer, SupplyDataBuffer, SupplyDataBuffer method [Microsoft TV Technologies], SupplyDataBuffer method [Microsoft TV Technologies],IMpeg2Stream interface, mpeg2data/IMpeg2Stream::SupplyDataBuffer, mstv.impeg2stream_supplydatabuffer
req.header: mpeg2data.h
req.include-header: 
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
 - IMpeg2Stream::SupplyDataBuffer
 - mpeg2data/IMpeg2Stream::SupplyDataBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - IMpeg2Stream.SupplyDataBuffer
---

# IMpeg2Stream::SupplyDataBuffer


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SupplyDataBuffer</b> method provides a buffer for the <b>Mpeg2Stream</b> object to write data.

## -parameters

### -param pStreamBuffer [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg_stream_buffer">MPEG_STREAM_BUFFER</a> structure allocated by the caller. This structure contains a pointer to the buffer, also allocated by the caller. The buffer must be at least 4096 bytes.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument or <b>NULL</b> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
</table>

## -remarks

The first time this method is called, it starts a worker thread that streams data to the buffer. When the data arrives, the <b>MPEG2Stream</b> object signals the event that was passed to the <a href="/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2stream-initialize">IMpeg2Stream::Initialize</a> method. (Typically an application specifies the event handle when it calls <a href="/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2data-getstreamofsections">IMpeg2Data::GetStreamOfSections</a>.)

When the event is signaled, examine the <b>hr</b> field of the <b>MPEG_STREAM_BUFFER</b> structure. If this value is a success code, the request was successful and the buffer contains valid data. To get more data, call the <b>SupplyDataBuffer</b> method again and wait for the event to be signaled.

The section headers are not converted from network byte order or otherwise processed.

If the object is still waiting for data, this method returns E_FAIL.

## -see-also

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2stream">IMpeg2Stream Interface</a>