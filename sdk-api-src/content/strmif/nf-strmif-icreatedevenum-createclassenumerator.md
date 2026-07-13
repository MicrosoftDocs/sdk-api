---
UID: NF:strmif.ICreateDevEnum.CreateClassEnumerator
title: ICreateDevEnum::CreateClassEnumerator (strmif.h)
description: The CreateClassEnumerator method creates an enumerator for a specified device category.
helpviewer_keywords: ["CreateClassEnumerator","CreateClassEnumerator method [DirectShow]","CreateClassEnumerator method [DirectShow]","ICreateDevEnum interface","ICreateDevEnum interface [DirectShow]","CreateClassEnumerator method","ICreateDevEnum.CreateClassEnumerator","ICreateDevEnum::CreateClassEnumerator","ICreateDevEnumCreateClassEnumerator","dshow.icreatedevenum_createclassenumerator","strmif/ICreateDevEnum::CreateClassEnumerator"]
old-location: dshow\icreatedevenum_createclassenumerator.htm
tech.root: dshow
ms.assetid: 07457acc-51f1-4d1b-b795-e8d980a5531e
ms.date: 4/26/2023
ms.keywords: CreateClassEnumerator, CreateClassEnumerator method [DirectShow], CreateClassEnumerator method [DirectShow],ICreateDevEnum interface, ICreateDevEnum interface [DirectShow],CreateClassEnumerator method, ICreateDevEnum.CreateClassEnumerator, ICreateDevEnum::CreateClassEnumerator, ICreateDevEnumCreateClassEnumerator, dshow.icreatedevenum_createclassenumerator, strmif/ICreateDevEnum::CreateClassEnumerator
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
 - ICreateDevEnum::CreateClassEnumerator
 - strmif/ICreateDevEnum::CreateClassEnumerator
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
 - ICreateDevEnum.CreateClassEnumerator
---

# ICreateDevEnum::CreateClassEnumerator


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>CreateClassEnumerator</b> method creates an enumerator for a specified device category.

## -parameters

### -param clsidDeviceClass [in]

Specifies the class identifier (CLSID) of the device category. See <a href="/windows/desktop/DirectShow/filter-categories">Filter Categories</a>.

### -param ppEnumMoniker [out]

Receives a pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ienummoniker">IEnumMoniker</a> interface. The caller must release the interface.

### -param dwFlags [in]

Bitwise combination of zero or more flags. If zero, the method enumerates every filter in the category. If any flags are set, the enumeration includes only filters that match the specified flags. The following flags are defined:

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>CDEF_DEVMON_CMGR_DEVICE</td>
<td>Enumerate audio or video codecs, using the audio compression manager (ACM) or video compression manager (VCM).</td>
</tr>
<tr>
<td>CDEF_DEVMON_DMO</td>
<td>Enumerate DirectX Media Objects (DMOs).</td>
</tr>
<tr>
<td>CDEF_DEVMON_FILTER</td>
<td>Enumerate native DirectShow filters.</td>
</tr>
<tr>
<td>CDEF_DEVMON_PNP_DEVICE</td>
<td>Enumerate Plug and Play hardware devices.</td>
</tr>
</table>

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The category specified by <i>clsidDeviceClass</i> does not exist or is empty.

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
</table>

## -remarks

If the category does not exist or is empty, the return value is S_FALSE, and the <i>ppEnumMoniker</i> parameter receives the value <b>NULL</b>. Therefore, test for the return value S_OK instead of using the <b>SUCCEEDED</b> macro:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IEnumMoniker *pEnum = NULL;
hr = pSysDevEnum-&gt;CreateClassEnumerator(
    CLSID_VideoCompressorCategory, &amp;pEnum, 0);
if (hr == S_OK) 
{
    // Safe to dereference pEnum.
    pEnum-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>
Use the <b>IEnumMoniker</b> interface to enumerate monikers that represent the filters in the device category. Monikers support the <b>IMoniker</b> interface. The monikers created by <b>CreateClassEnumerator</b> also support the <a href="/windows/desktop/api/strmif/nn-strmif-igetcapabilitieskey">IGetCapabilitiesKey</a> interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icreatedevenum">ICreateDevEnum Interface</a>