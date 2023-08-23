---
UID: NF:strmif.IDvdInfo2.GetDVDVolumeInfo
title: IDvdInfo2::GetDVDVolumeInfo (strmif.h)
description: The GetDVDVolumeInfo method retrieves the current DVD volume information.
helpviewer_keywords: ["GetDVDVolumeInfo","GetDVDVolumeInfo method [DirectShow]","GetDVDVolumeInfo method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetDVDVolumeInfo method","IDvdInfo2.GetDVDVolumeInfo","IDvdInfo2::GetDVDVolumeInfo","IDvdInfo2GetDVDVolumeInfo","dshow.idvdinfo2_getdvdvolumeinfo","strmif/IDvdInfo2::GetDVDVolumeInfo"]
old-location: dshow\idvdinfo2_getdvdvolumeinfo.htm
tech.root: dshow
ms.assetid: d55973af-5f56-4e22-b3b0-2cee9f57c2d4
ms.date: 4/26/2023
ms.keywords: GetDVDVolumeInfo, GetDVDVolumeInfo method [DirectShow], GetDVDVolumeInfo method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDVDVolumeInfo method, IDvdInfo2.GetDVDVolumeInfo, IDvdInfo2::GetDVDVolumeInfo, IDvdInfo2GetDVDVolumeInfo, dshow.idvdinfo2_getdvdvolumeinfo, strmif/IDvdInfo2::GetDVDVolumeInfo
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
 - IDvdInfo2::GetDVDVolumeInfo
 - strmif/IDvdInfo2::GetDVDVolumeInfo
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
 - IDvdInfo2.GetDVDVolumeInfo
---

# IDvdInfo2::GetDVDVolumeInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDVDVolumeInfo</code> method retrieves the current DVD volume information.

## -parameters

### -param pulNumOfVolumes [out]

Receives the number of volumes in the volume set.

### -param pulVolume [out]

Receives the volume number for this root directory.

### -param pSide [out]

Pointer to a variable of type [DVD_DISC_SIDE](/windows/desktop/api/strmif/ne-strmif-dvd_disc_side) that receives the current disc side.

### -param pulNumOfTitles [out]

Pointer to a variable of type ULONG that receives the number of titles available in this volume.

## -returns

Returns one of the following <b>HRESULT</b> values.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>

## -remarks

Some discs can be distributed as part of multidisc set. "Volume" in this context can mean either "disc" or "disc side", depending on how the disc was authored.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>