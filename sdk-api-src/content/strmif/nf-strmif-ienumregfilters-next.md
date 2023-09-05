---
UID: NF:strmif.IEnumRegFilters.Next
title: IEnumRegFilters::Next (strmif.h)
description: Note  The IEnumRegFilters interface is deprecated. Fills the array with descriptions of the next set of filters (specified by the cFilters parameter) that meet the requirements specified upon creation of the enumerator.
helpviewer_keywords: ["IEnumRegFilters interface [DirectShow]","Next method","IEnumRegFilters.Next","IEnumRegFilters::Next","IEnumRegFiltersNext","Next","Next method [DirectShow]","Next method [DirectShow]","IEnumRegFilters interface","dshow.ienumregfilters_next","strmif/IEnumRegFilters::Next"]
old-location: dshow\ienumregfilters_next.htm
tech.root: dshow
ms.assetid: ec255b9b-33cf-42a3-9f02-f1f34eee2da1
ms.date: 4/26/2023
ms.keywords: IEnumRegFilters interface [DirectShow],Next method, IEnumRegFilters.Next, IEnumRegFilters::Next, IEnumRegFiltersNext, Next, Next method [DirectShow], Next method [DirectShow],IEnumRegFilters interface, dshow.ienumregfilters_next, strmif/IEnumRegFilters::Next
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumRegFilters::Next
 - strmif/IEnumRegFilters::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IEnumRegFilters.Next
---

# IEnumRegFilters::Next


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IEnumRegFilters</b> interface is deprecated.</div>
<div> </div>
Fills the array with descriptions of the next set of filters (specified by the <i>cFilters</i> parameter) that meet the requirements specified upon creation of the enumerator.

## -parameters

### -param cFilters [in]

Number of filters.

### -param apRegFilter [out]

Address of a pointer to an array of <b>REGFILTER</b> pointers.

### -param pcFetched [out]

Pointer to the actual number of filters passed.

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
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Fewer filters were retrieved than requested.

</td>
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
<dt><b>VFW_E_ENUM_OUT_OF_SYNC</b></dt>
</dl>
</td>
<td width="60%">
The enumerator has become invalid. For more information, see Remarks.

</td>
</tr>
</table>

## -remarks

The calling application must use the Microsoft Win32 <b>CoTaskMemFree</b> function to free each <b>REGFILTER</b> pointer returned in the array. Do not free the <b>Name</b> member of the <b>REGFILTER</b> structure separately, because <code>IEnumRegFilters::Next</code> allocates memory for this string as part of the <b>REGFILTER</b> structure.

If the number of registered filters changes, the state of the enumerator will no longer be consistent with the state of the registry. As a result, this method will return VFW_E_ENUM_OUT_OF_SYNC. You should discard any data obtained from previous calls to the enumerator, because it might be invalid, and update the enumerator by calling the <a href="/windows/desktop/api/strmif/nf-strmif-ienumregfilters-reset">Reset</a> method. You can then call the <code>Next</code> method safely.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ienumregfilters">IEnumRegFilters Interface</a>