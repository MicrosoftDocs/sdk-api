---
UID: NF:strmif.IDvdInfo2.GetMenuLanguages
title: IDvdInfo2::GetMenuLanguages (strmif.h)
description: The GetMenuLanguages method retrieves all the languages available for all menus on the disc.
helpviewer_keywords: ["GetMenuLanguages","GetMenuLanguages method [DirectShow]","GetMenuLanguages method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetMenuLanguages method","IDvdInfo2.GetMenuLanguages","IDvdInfo2::GetMenuLanguages","IDvdInfo2GetMenuLanguages","dshow.idvdinfo2_getmenulanguages","strmif/IDvdInfo2::GetMenuLanguages"]
old-location: dshow\idvdinfo2_getmenulanguages.htm
tech.root: dshow
ms.assetid: 97c95208-e2fc-4c9a-b8ba-61419b96aec9
ms.date: 4/26/2023
ms.keywords: GetMenuLanguages, GetMenuLanguages method [DirectShow], GetMenuLanguages method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetMenuLanguages method, IDvdInfo2.GetMenuLanguages, IDvdInfo2::GetMenuLanguages, IDvdInfo2GetMenuLanguages, dshow.idvdinfo2_getmenulanguages, strmif/IDvdInfo2::GetMenuLanguages
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
 - IDvdInfo2::GetMenuLanguages
 - strmif/IDvdInfo2::GetMenuLanguages
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
 - IDvdInfo2.GetMenuLanguages
---

# IDvdInfo2::GetMenuLanguages


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetMenuLanguages</code> method retrieves all the languages available for all menus on the disc.

## -parameters

### -param pLanguages [out]

Pointer to an <b>LCID</b> array that receives the languages returned. To retrieve only the number of languages available for menus, and not the actual languages themselves, specify <b>NULL</b> for <i>pLanguages</i>.

### -param ulMaxLanguages [in]

Maximum number of languages to retrieve.

### -param pulActualLanguages [out]

Receives the actual number of languages retrieved.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not initialized.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>