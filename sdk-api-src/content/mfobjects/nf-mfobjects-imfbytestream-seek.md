---
UID: NF:mfobjects.IMFByteStream.Seek
title: IMFByteStream::Seek (mfobjects.h)
description: Moves the current position in the stream by a specified offset.
helpviewer_keywords: ["512c67a5-e87d-4a81-8577-e64dac868c40","IMFByteStream interface [Media Foundation]","Seek method","IMFByteStream.Seek","IMFByteStream::Seek","MFBYTESTREAM_SEEK_FLAG_CANCEL_PENDING_IO","Seek","Seek method [Media Foundation]","Seek method [Media Foundation]","IMFByteStream interface","mf.imfbytestream_seek","mfobjects/IMFByteStream::Seek"]
old-location: mf\imfbytestream_seek.htm
tech.root: mf
ms.assetid: 512c67a5-e87d-4a81-8577-e64dac868c40
ms.date: 12/05/2018
ms.keywords: 512c67a5-e87d-4a81-8577-e64dac868c40, IMFByteStream interface [Media Foundation],Seek method, IMFByteStream.Seek, IMFByteStream::Seek, MFBYTESTREAM_SEEK_FLAG_CANCEL_PENDING_IO, Seek, Seek method [Media Foundation], Seek method [Media Foundation],IMFByteStream interface, mf.imfbytestream_seek, mfobjects/IMFByteStream::Seek
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - IMFByteStream::Seek
 - mfobjects/IMFByteStream::Seek
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
 - IMFByteStream.Seek
---

# IMFByteStream::Seek


## -description

Moves the current position in the stream by a specified offset.

## -parameters

### -param SeekOrigin [in]

Specifies the origin of the seek as a member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mfbytestream_seek_origin">MFBYTESTREAM_SEEK_ORIGIN</a> enumeration. The offset is calculated relative to this position.

### -param llSeekOffset [in]

Specifies the new position, as a byte offset from the seek origin.

### -param dwSeekFlags [in]

Specifies zero or more flags. The following flags are defined.
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFBYTESTREAM_SEEK_FLAG_CANCEL_PENDING_IO"></a><a id="mfbytestream_seek_flag_cancel_pending_io"></a><dl>
<dt><b>MFBYTESTREAM_SEEK_FLAG_CANCEL_PENDING_IO</b></dt>
</dl>
</td>
<td width="60%">
All pending I/O requests are canceled after the seek request completes successfully.
              

</td>
</tr>
</table>

### -param pqwCurrentPosition [out]

Receives the new position after the seek.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>
<b> Implementation notes:</b> This method should update the current position in the stream by adding the <i>qwSeekOffset</i> to the seek <i>SeekOrigin</i> position. This should be the same value passed back in the <i>pqwCurrentPosition</i> parameter. 
Other methods that can update the current position are <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read">Read</a>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread">BeginRead</a>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write">Write</a>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginwrite">BeginWrite</a>, and <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-setcurrentposition">SetCurrentPosition</a>.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>