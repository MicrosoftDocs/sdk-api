---
UID: NF:strmif.IDvdControl2.PlayForwards
title: IDvdControl2::PlayForwards (strmif.h)
description: The PlayForwards method plays forward at the specified speed from the current location.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","PlayForwards method","IDvdControl2.PlayForwards","IDvdControl2::PlayForwards","IDvdControl2PlayForwards","PlayForwards","PlayForwards method [DirectShow]","PlayForwards method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_playforwards","strmif/IDvdControl2::PlayForwards"]
old-location: dshow\idvdcontrol2_playforwards.htm
tech.root: dshow
ms.assetid: bf57e2fd-c85f-430d-a1fa-5b59f7bfb8af
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],PlayForwards method, IDvdControl2.PlayForwards, IDvdControl2::PlayForwards, IDvdControl2PlayForwards, PlayForwards, PlayForwards method [DirectShow], PlayForwards method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_playforwards, strmif/IDvdControl2::PlayForwards
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
 - IDvdControl2::PlayForwards
 - strmif/IDvdControl2::PlayForwards
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
 - IDvdControl2.PlayForwards
---

# IDvdControl2::PlayForwards


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>PlayForwards</code> method plays forward at the specified speed from the current location.

## -parameters

### -param dSpeed [in]

Value that specifies the playback speed. This value is a multiplier, where 1.0 is the authored speed, so a value of 2.5 plays at two and one-half times the authored speed, while a value of 0.5 plays at half the authored speed. The actual speed of playback depends on the capabilities of the video decoder. Values below 0.00001 are converted to 0.00001.

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

This method is demonstrated in the DVDSample application in <b>CDvdCore::FastForward</b>.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Forward_Scan</td>
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