---
UID: NF:strmif.IDvdControl2.SetDVDDirectory
title: IDvdControl2::SetDVDDirectory (strmif.h)
description: The SetDVDDirectory method sets the DVD drive that the DVD Navigator filter will read from.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","SetDVDDirectory method","IDvdControl2.SetDVDDirectory","IDvdControl2::SetDVDDirectory","IDvdControl2SetDVDDirectory","SetDVDDirectory","SetDVDDirectory method [DirectShow]","SetDVDDirectory method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_setdvddirectory","strmif/IDvdControl2::SetDVDDirectory"]
old-location: dshow\idvdcontrol2_setdvddirectory.htm
tech.root: dshow
ms.assetid: fa64a614-14cb-4ea9-a005-0e738490b6d6
ms.date: 4/26/2023
ms.keywords: IDvdControl2 interface [DirectShow],SetDVDDirectory method, IDvdControl2.SetDVDDirectory, IDvdControl2::SetDVDDirectory, IDvdControl2SetDVDDirectory, SetDVDDirectory, SetDVDDirectory method [DirectShow], SetDVDDirectory method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_setdvddirectory, strmif/IDvdControl2::SetDVDDirectory
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
 - IDvdControl2::SetDVDDirectory
 - strmif/IDvdControl2::SetDVDDirectory
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
 - IDvdControl2.SetDVDDirectory
---

# IDvdControl2::SetDVDDirectory


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetDVDDirectory</code> method sets the DVD drive that the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter will read from.

## -parameters

### -param pszwPath [in]

Pointer to a wide-character string that specifies the path of the root directory.

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
The <i>pszwPath</i> parameter points to an invalid DVD path, or a DVD drive is not found while enumerating.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The DVD Navigator is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Invalid domain. For details, see Remarks.

</td>
</tr>
</table>

## -remarks

If <i>pszwPath</i> is <b>NULL</b>, the DVD Navigator tries to select a DVD volume on any available drive. On startup, the DVD Navigator automatically looks for a drive, starting at drive C, with a VIDEO_TS folder in the root folder. It is therefore only necessary to call <code>SetDVDDirectory</code> when you have more than one DVD drive on a machine, or if your DVD drive letter is A or B. When specifying the path, include the video_ts folder.

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
SetDVDDirectory(L"e:\\video_ts");
</pre>
</td>
</tr>
</table></span></div>
Some DVD volumes may have their video in a directory named something other than "video_ts." The general idea is that an additional "DVD volume" (the set of .IFO. VOB, and .BUP files that would normally be stored in the VIDEO_TS directory) can be placed in a subdirectory on the disc. By changing the root to point to this directory, MSWebDVD will operate on this separate DVD volume. A new set of menus, titles, and so on will be available, independent of the titles in the VIDEO_TS root, which will no longer be accessible. Such directories are called "hidden directories." The following example shows how to set a hidden directory as the root, where "hidden" is a placeholder for whatever name the disc authors have given to the directory.

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
SetDVDDirectory(L"d:\\webdvd\\hidden");
</pre>
</td>
</tr>
</table></span></div>
If the filter graph is running and the DVD Navigator finds a DVD in the directory specified by <i>pszwPath</i>, the DVD Navigator automatically begins playing the disc. This conforms with the DVD specification and ensures that the new disc is initialized properly. If you do not want the new disc to play automatically after <code>SetDVDDirectory</code> returns, you must set the DVD_ResetOnStop flag in <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setoption">IDvdControl2::SetOption</a> to <b>TRUE</b> and stop the filter graph through a call to <a href="/windows/desktop/api/control/nf-control-imediacontrol-stop">IMediaControl::Stop</a> on the Filter Graph Manager. If DVD_ResetOnStop is set to <b>FALSE</b>, then <code>SetDVDDirectory</code> returns VFW_E_DVD_INVALIDDOMAIN.

This method is demonstrated in the DVDSample application in <b>CDvdCore::SetDirectory</b>.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>None</td>
<td>DVD_DOMAIN_Stop</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>