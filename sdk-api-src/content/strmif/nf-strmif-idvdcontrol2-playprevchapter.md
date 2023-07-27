---
UID: NF:strmif.IDvdControl2.PlayPrevChapter
title: IDvdControl2::PlayPrevChapter (strmif.h)
description: The PlayPrevChapter method starts playback from the beginning of the previous chapter in the current title.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","PlayPrevChapter method","IDvdControl2.PlayPrevChapter","IDvdControl2::PlayPrevChapter","IDvdControl2PlayPrevChapter","PlayPrevChapter","PlayPrevChapter method [DirectShow]","PlayPrevChapter method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_playprevchapter","strmif/IDvdControl2::PlayPrevChapter"]
old-location: dshow\idvdcontrol2_playprevchapter.htm
tech.root: dshow
ms.assetid: bebfe1e1-9197-4105-9b3f-edeb6f04836c
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],PlayPrevChapter method, IDvdControl2.PlayPrevChapter, IDvdControl2::PlayPrevChapter, IDvdControl2PlayPrevChapter, PlayPrevChapter, PlayPrevChapter method [DirectShow], PlayPrevChapter method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_playprevchapter, strmif/IDvdControl2::PlayPrevChapter
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
 - IDvdControl2::PlayPrevChapter
 - strmif/IDvdControl2::PlayPrevChapter
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
 - IDvdControl2.PlayPrevChapter
---

# IDvdControl2::PlayPrevChapter


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>PlayPrevChapter</code> method starts playback from the beginning of the previous chapter in the current title.

## -parameters

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
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
</table>

## -remarks

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

This method is demonstrated in the DVDSample application in <b>CDvdCore::PrevChapter</b>.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>PrevPG_Search</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
</ul>
</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>