---
UID: NF:mfobjects.IMFByteStream.GetCapabilities
title: IMFByteStream::GetCapabilities (mfobjects.h)
description: Retrieves the characteristics of the byte stream.
helpviewer_keywords: ["715e802b-4707-4c6d-9ae9-a4ddfa90f05e","GetCapabilities","GetCapabilities method [Media Foundation]","GetCapabilities method [Media Foundation]","IMFByteStream interface","IMFByteStream interface [Media Foundation]","GetCapabilities method","IMFByteStream.GetCapabilities","IMFByteStream::GetCapabilities","MFBYTESTREAM_DOES_NOT_USE_NETWORK","MFBYTESTREAM_HAS_SLOW_SEEK","MFBYTESTREAM_IS_DIRECTORY","MFBYTESTREAM_IS_PARTIALLY_DOWNLOADED","MFBYTESTREAM_IS_READABLE","MFBYTESTREAM_IS_REMOTE","MFBYTESTREAM_IS_SEEKABLE","MFBYTESTREAM_IS_WRITABLE","MFBYTESTREAM_SHARE_WRITE","mf.imfbytestream_getcapabilities","mfobjects/IMFByteStream::GetCapabilities"]
old-location: mf\imfbytestream_getcapabilities.htm
tech.root: mf
ms.assetid: 715e802b-4707-4c6d-9ae9-a4ddfa90f05e
ms.date: 12/05/2018
ms.keywords: 715e802b-4707-4c6d-9ae9-a4ddfa90f05e, GetCapabilities, GetCapabilities method [Media Foundation], GetCapabilities method [Media Foundation],IMFByteStream interface, IMFByteStream interface [Media Foundation],GetCapabilities method, IMFByteStream.GetCapabilities, IMFByteStream::GetCapabilities, MFBYTESTREAM_DOES_NOT_USE_NETWORK, MFBYTESTREAM_HAS_SLOW_SEEK, MFBYTESTREAM_IS_DIRECTORY, MFBYTESTREAM_IS_PARTIALLY_DOWNLOADED, MFBYTESTREAM_IS_READABLE, MFBYTESTREAM_IS_REMOTE, MFBYTESTREAM_IS_SEEKABLE, MFBYTESTREAM_IS_WRITABLE, MFBYTESTREAM_SHARE_WRITE, mf.imfbytestream_getcapabilities, mfobjects/IMFByteStream::GetCapabilities
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
 - IMFByteStream::GetCapabilities
 - mfobjects/IMFByteStream::GetCapabilities
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
 - IMFByteStream.GetCapabilities
---

# IMFByteStream::GetCapabilities


## -description

Retrieves the characteristics of the byte stream.

## -parameters

### -param pdwCapabilities [out]

Receives a bitwise <b>OR</b> of zero or more flags. The following flags are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MFBYTESTREAM_IS_READABLE"></a><a id="mfbytestream_is_readable"></a><dl>
<dt><b>MFBYTESTREAM_IS_READABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The byte stream can be read.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MFBYTESTREAM_IS_WRITABLE"></a><a id="mfbytestream_is_writable"></a><dl>
<dt><b>MFBYTESTREAM_IS_WRITABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The byte stream can be written to.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MFBYTESTREAM_IS_SEEKABLE"></a><a id="mfbytestream_is_seekable"></a><dl>
<dt><b>MFBYTESTREAM_IS_SEEKABLE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The byte stream can be seeked.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MFBYTESTREAM_IS_REMOTE"></a><a id="mfbytestream_is_remote"></a><dl>
<dt><b>MFBYTESTREAM_IS_REMOTE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The byte stream is from a remote source, such as a network.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MFBYTESTREAM_IS_DIRECTORY"></a><a id="mfbytestream_is_directory"></a><dl>
<dt><b>MFBYTESTREAM_IS_DIRECTORY</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The byte stream represents a file directory.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MFBYTESTREAM_HAS_SLOW_SEEK"></a><a id="mfbytestream_has_slow_seek"></a><dl>
<dt><b>MFBYTESTREAM_HAS_SLOW_SEEK</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Seeking within this stream might be slow. For example, the byte stream might download from a network.

</td>
</tr>
<tr>
<td width="40%"><a id="MFBYTESTREAM_IS_PARTIALLY_DOWNLOADED"></a><a id="mfbytestream_is_partially_downloaded"></a><dl>
<dt><b>MFBYTESTREAM_IS_PARTIALLY_DOWNLOADED</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The byte stream is currently downloading data to a local cache.
              Read operations on the byte stream might take longer until the data is completely downloaded.

This flag is cleared after all of the data has been downloaded.

If the <b>MFBYTESTREAM_HAS_SLOW_SEEK</b> flag is also set, it means the byte stream must download the entire file sequentially. Otherwise, the byte stream can respond to seek requests by restarting the download from a new point in the stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MFBYTESTREAM_SHARE_WRITE"></a><a id="mfbytestream_share_write"></a><dl>
<dt><b>MFBYTESTREAM_SHARE_WRITE</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Another thread or process can open this byte stream for writing. If this flag is present, the length of the
byte stream could change while it is being read. 

This flag can affect the behavior of byte-stream handlers. For more information, see <a href="/windows/desktop/medfound/mf-bytestreamhandler-accepts-share-write">MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE</a>.

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="MFBYTESTREAM_DOES_NOT_USE_NETWORK"></a><a id="mfbytestream_does_not_use_network"></a><dl>
<dt><b>MFBYTESTREAM_DOES_NOT_USE_NETWORK</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
The byte stream is not currently
using the network to receive the content.  Networking hardware
may enter a power saving state when this bit is set.

<div class="alert"><b>Note</b>  Requires Windows 8 or later.</div>
<div> </div>
</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>