---
UID: NF:strmif.IDvdControl2.SelectSubpictureStream
title: IDvdControl2::SelectSubpictureStream (strmif.h)
description: The SelectSubpictureStream method sets the subpicture stream to display.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","SelectSubpictureStream method","IDvdControl2.SelectSubpictureStream","IDvdControl2::SelectSubpictureStream","IDvdControl2SelectSubpictureStream","SelectSubpictureStream","SelectSubpictureStream method [DirectShow]","SelectSubpictureStream method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_selectsubpicturestream","strmif/IDvdControl2::SelectSubpictureStream"]
old-location: dshow\idvdcontrol2_selectsubpicturestream.htm
tech.root: dshow
ms.assetid: 0553a0c4-34d3-4774-9a22-acc01c0a832a
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],SelectSubpictureStream method, IDvdControl2.SelectSubpictureStream, IDvdControl2::SelectSubpictureStream, IDvdControl2SelectSubpictureStream, SelectSubpictureStream, SelectSubpictureStream method [DirectShow], SelectSubpictureStream method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectsubpicturestream, strmif/IDvdControl2::SelectSubpictureStream
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdControl2::SelectSubpictureStream
 - strmif/IDvdControl2::SelectSubpictureStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdControl2.SelectSubpictureStream
---

# IDvdControl2::SelectSubpictureStream


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SelectSubpictureStream</code> method sets the subpicture stream to display.

## -parameters

### -param ulSubPicture

Value that specifies the subpicture stream, which must be from 0 through 31, or 63.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0-31</td>
<td>The stream is valid.</td>
</tr>
<tr>
<td>63</td>
<td>The stream is the <i>dummy stream</i>, which means it is a muted, low-bitrate stream.</td>
</tr>
</table>

### -param dwFlags [in]

Bitwise OR of one or more flags from the <a href="/windows/desktop/api/strmif/ne-strmif-dvd_cmd_flags">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.

### -param ppCmd [out]

Receives a pointer to an <a href="/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>.

## -returns

Returns one of the following values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ulSubPicture</i> is out of range or doesn't correspond to an SP stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>ulSubPicture</i> parameter is valid, but DVD Navigator cannot set it for some other reason.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Invalid domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_STREAM_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The specified stream is disabled.

</td>
</tr>
</table>

## -remarks

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Sub-picture_Stream_Change</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
<li>DVD_DOMAIN_Stop</li>
</ul>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/audio-and-subpicture-streams">Audio and Subpicture Streams</a>



<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>