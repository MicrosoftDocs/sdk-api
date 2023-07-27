---
UID: NF:strmif.IDvdControl2.PlayChaptersAutoStop
title: IDvdControl2::PlayChaptersAutoStop (strmif.h)
description: The PlayChaptersAutoStop method plays the number of chapters specified, starting at the specified chapter within the specified title.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","PlayChaptersAutoStop method","IDvdControl2.PlayChaptersAutoStop","IDvdControl2::PlayChaptersAutoStop","IDvdControl2PlayChaptersAutoStop","PlayChaptersAutoStop","PlayChaptersAutoStop method [DirectShow]","PlayChaptersAutoStop method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_playchaptersautostop","strmif/IDvdControl2::PlayChaptersAutoStop"]
old-location: dshow\idvdcontrol2_playchaptersautostop.htm
tech.root: dshow
ms.assetid: fdf9642b-ac90-4ffc-a813-4a5b22a973dd
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],PlayChaptersAutoStop method, IDvdControl2.PlayChaptersAutoStop, IDvdControl2::PlayChaptersAutoStop, IDvdControl2PlayChaptersAutoStop, PlayChaptersAutoStop, PlayChaptersAutoStop method [DirectShow], PlayChaptersAutoStop method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_playchaptersautostop, strmif/IDvdControl2::PlayChaptersAutoStop
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
 - IDvdControl2::PlayChaptersAutoStop
 - strmif/IDvdControl2::PlayChaptersAutoStop
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
 - IDvdControl2.PlayChaptersAutoStop
---

# IDvdControl2::PlayChaptersAutoStop


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>PlayChaptersAutoStop</code> method plays the number of chapters specified, starting at the specified chapter within the specified title.

## -parameters

### -param ulTitle [in]

Value that specifies the title in which the chapter is located; this value must be from 1 through 99.

### -param ulChapter [in]

Value that specifies the chapter in the specified title where the DVD Navigator will start playback; this value must be from 1 through 999.

### -param ulChaptersToPlay [in]

Number of chapters to play from the start chapter.

### -param dwFlags [in]

Bitwise <b>OR</b> of one or more flags from the <a href="/windows/desktop/api/strmif/ne-strmif-dvd_cmd_flags">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The DVD Navigator is not initialized or the title is not a One Sequential PGC Title.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ulTitle</i> value does not exist or is greater than the number of titles, or <i>ulChapter</i> does not exist or is greater than the number of chapters, or <i>ulChapter</i> plus <i>ulChaptersToPlay</i> is greater than the number of chapters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_GRAPHNOTREADY</b></dt>
</dl>
</td>
<td width="60%">
The graph is not in a running state.

</td>
</tr>
</table>

## -remarks

This method works only on One_Sequential_PGC_Titles. When the specified number of chapters have been played, the DVD Navigator sends the application an <a href="/windows/desktop/DirectShow/ec-dvd-chapter-autostop">EC_DVD_CHAPTER_AUTOSTOP</a> event notification.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>None.</td>
<td>All.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>