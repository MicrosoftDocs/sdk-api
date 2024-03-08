---
UID: NF:strmif.IDvdInfo2.GetSubpictureLanguage
title: IDvdInfo2::GetSubpictureLanguage (strmif.h)
description: The GetSubpictureLanguage method retrieves the language of the specified subpicture stream within the current title.
helpviewer_keywords: ["GetSubpictureLanguage","GetSubpictureLanguage method [DirectShow]","GetSubpictureLanguage method [DirectShow]","IDvdInfo2 interface","IDvdInfo2 interface [DirectShow]","GetSubpictureLanguage method","IDvdInfo2.GetSubpictureLanguage","IDvdInfo2::GetSubpictureLanguage","IDvdInfo2GetSubpictureLanguage","dshow.idvdinfo2_getsubpicturelanguage","strmif/IDvdInfo2::GetSubpictureLanguage"]
old-location: dshow\idvdinfo2_getsubpicturelanguage.htm
tech.root: dshow
ms.assetid: 175ab238-59a9-4142-921b-ed374423f4e3
ms.date: 4/26/2023
ms.keywords: GetSubpictureLanguage, GetSubpictureLanguage method [DirectShow], GetSubpictureLanguage method [DirectShow],IDvdInfo2 interface, IDvdInfo2 interface [DirectShow],GetSubpictureLanguage method, IDvdInfo2.GetSubpictureLanguage, IDvdInfo2::GetSubpictureLanguage, IDvdInfo2GetSubpictureLanguage, dshow.idvdinfo2_getsubpicturelanguage, strmif/IDvdInfo2::GetSubpictureLanguage
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
 - IDvdInfo2::GetSubpictureLanguage
 - strmif/IDvdInfo2::GetSubpictureLanguage
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
 - IDvdInfo2.GetSubpictureLanguage
---

# IDvdInfo2::GetSubpictureLanguage


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetSubpictureLanguage</code> method retrieves the language of the specified subpicture stream within the current title.

## -parameters

### -param ulStream [in]

Number of the subpicture stream for which the language is being retrieved.

### -param pLanguage [out]

Pointer to an LCID that receives the locale information. The language information can then be extracted from the LCID by using the Win32 <b>MAKELANGID</b> macro.

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
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> is not initialized or not in a valid domain.

</td>
</tr>
</table>

## -remarks

To get the text languages available for a menu, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getmenulanguages">GetMenuLanguages</a>. <code>GetSubpictureLanguage</code> sets the value pointed to by <i>pLanguage</i> to zero if the stream contains an unknown language. Call the Win32 <b>GetLocaleInfo</b> function as follows to create a human-readable string name from <i>pLanguage</i>:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
LCID Language;
hr = pDvdInfo-&gt;GetSubpictureLanguage(ulStream, &amp;Language);
if (SUCCEEDED(hr))
{
    int cchSize = GetLocaleInfo(Language, LOCALE_SENGLANGUAGE, 0, 0);
    TCHAR *szString = new TCHAR[cchSize];
    if (szString)
    {
        GetLocaleInfo(Language, LOCALE_SENGLANGUAGE, szString, cchSize);
        /* ... */
        delete [] szString;
    }
}
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2 Interface</a>