---
UID: NF:strmif.IFileSinkFilter.GetCurFile
title: IFileSinkFilter::GetCurFile (strmif.h)
description: The GetCurFile method retrieves the name and media type of the current file. (IFileSinkFilter.GetCurFile)
helpviewer_keywords: ["GetCurFile","GetCurFile method [DirectShow]","GetCurFile method [DirectShow]","IFileSinkFilter interface","IFileSinkFilter interface [DirectShow]","GetCurFile method","IFileSinkFilter.GetCurFile","IFileSinkFilter::GetCurFile","IFileSinkFilterGetCurFile","dshow.ifilesinkfilter_getcurfile","strmif/IFileSinkFilter::GetCurFile"]
old-location: dshow\ifilesinkfilter_getcurfile.htm
tech.root: dshow
ms.assetid: 1d635dfc-a3b3-4f75-8356-534a32156686
ms.date: 4/26/2023
ms.keywords: GetCurFile, GetCurFile method [DirectShow], GetCurFile method [DirectShow],IFileSinkFilter interface, IFileSinkFilter interface [DirectShow],GetCurFile method, IFileSinkFilter.GetCurFile, IFileSinkFilter::GetCurFile, IFileSinkFilterGetCurFile, dshow.ifilesinkfilter_getcurfile, strmif/IFileSinkFilter::GetCurFile
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IFileSinkFilter::GetCurFile
 - strmif/IFileSinkFilter::GetCurFile
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
 - IFileSinkFilter.GetCurFile
---

# IFileSinkFilter::GetCurFile


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCurFile</code> method retrieves the name and media type of the current file.

## -parameters

### -param ppszFileName [out]

Address of a pointer that receives the name of the file, as an <b>OLESTR</b> type.

### -param pmt [out]

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that receives the media type. This parameter can by <b>NULL</b>, in which case the method does not return the media type.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No file is opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument in <i>ppszFileName</i>.

</td>
</tr>
</table>

## -remarks

If the filter has not opened a file, the method might succeed but return <b>NULL</b> in the <i>ppszFileName</i> parameter. Check the value when the method returns.

The method allocates the memory for the string returned in <i>ppszFileName</i>, and the memory for the format block in the media type (if any). The caller must free them by calling <b>CoTaskMemFree</b>. For the media type, you can use the <a href="/windows/desktop/DirectShow/freemediatype">FreeMediaType</a> function in the base class library.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ifilesinkfilter">IFileSinkFilter Interface</a>
