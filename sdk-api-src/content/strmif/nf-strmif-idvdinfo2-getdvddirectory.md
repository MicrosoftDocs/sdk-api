---
UID: NF:strmif.IDvdInfo2.GetDVDDirectory
title: IDvdInfo2::GetDVDDirectory (strmif.h)
description: The GetDVDDirectory method retrieves the root directory that is set in the DVD Navigator.
helpviewer_keywords: ["GetDVDDirectory","GetDVDDirectory method [DirectShow]","GetDVDDirectory method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetDVDDirectory method","IDvdInfo2.GetDVDDirectory","IDvdInfo2::GetDVDDirectory","IDvdInfo2GetDVDDirectory","dshow.idvdinfo2_getdvddirectory","strmif/IDvdInfo2::GetDVDDirectory"]
old-location: dshow\idvdinfo2_getdvddirectory.htm
tech.root: dshow
ms.assetid: fad4dd0a-4831-4460-9631-ed06b6647f2d
ms.date: 4/26/2023
ms.keywords: GetDVDDirectory, GetDVDDirectory method [DirectShow], GetDVDDirectory method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetDVDDirectory method, IDvdInfo2.GetDVDDirectory, IDvdInfo2::GetDVDDirectory, IDvdInfo2GetDVDDirectory, dshow.idvdinfo2_getdvddirectory, strmif/IDvdInfo2::GetDVDDirectory
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
 - IDvdInfo2::GetDVDDirectory
 - strmif/IDvdInfo2::GetDVDDirectory
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
 - IDvdInfo2.GetDVDDirectory
---

# IDvdInfo2::GetDVDDirectory


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetDVDDirectory</code> method retrieves the root directory that is set in the DVD Navigator.

## -parameters

### -param pszwPath [out]

Pointer to a buffer that receives the path string.

### -param ulMaxSize [in]

Size of the buffer, in WCHARs.

### -param pulActualSize [out]

Pointer to a variable that receives the size of actual data returned, in WCHARs.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to hold the string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not in a valid domain.

</td>
</tr>
</table>

## -remarks

This method is demonstrated in the DVDSample application in <b>CDvdCore::GetDriveLetter</b>.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>