---
UID: NF:strmif.ICaptureGraphBuilder2.FindInterface
title: ICaptureGraphBuilder2::FindInterface (strmif.h)
description: The FindInterface method searches the graph for a specified interface, starting from a specified filter.
helpviewer_keywords: ["FindInterface","FindInterface method [DirectShow]","FindInterface method [DirectShow]","ICaptureGraphBuilder2 interface","ICaptureGraphBuilder2 interface [DirectShow]","FindInterface method","ICaptureGraphBuilder2.FindInterface","ICaptureGraphBuilder2::FindInterface","ICaptureGraphBuilder2FindInterface","dshow.icapturegraphbuilder2_findinterface","strmif/ICaptureGraphBuilder2::FindInterface"]
old-location: dshow\icapturegraphbuilder2_findinterface.htm
tech.root: dshow
ms.assetid: 931b42bf-25d6-4f0a-8c45-baf8ed65e302
ms.date: 4/26/2023
ms.keywords: FindInterface, FindInterface method [DirectShow], FindInterface method [DirectShow],ICaptureGraphBuilder2 interface, ICaptureGraphBuilder2 interface [DirectShow],FindInterface method, ICaptureGraphBuilder2.FindInterface, ICaptureGraphBuilder2::FindInterface, ICaptureGraphBuilder2FindInterface, dshow.icapturegraphbuilder2_findinterface, strmif/ICaptureGraphBuilder2::FindInterface
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
 - ICaptureGraphBuilder2::FindInterface
 - strmif/ICaptureGraphBuilder2::FindInterface
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
 - ICaptureGraphBuilder2.FindInterface
---

# ICaptureGraphBuilder2::FindInterface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>FindInterface</code> method searches the graph for a specified interface, starting from a specified filter. You can restrict the search to a section of the graph upstream or downstream of the filter, or restrict it to a particular pin category or media type.

## -parameters

### -param pCategory [in]

A pointer to a GUID that specifies the search criteria. See Remarks for more information. The following values are possible:

<ul>
<li>&amp;LOOK_UPSTREAM_ONLY.</li>
<li>&amp;LOOK_DOWNSTREAM_ONLY.</li>
<li>One of the pin categories listed in <a href="/windows/desktop/DirectShow/pin-property-set">Pin Property Set</a>. </li>
<li><b>NULL</b></li>
</ul>
See Remarks for more information.

### -param pType [in]

Pointer to a GUID that specifies the major media type of an output pin, or <b>NULL</b>.

### -param pf [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface of the filter. The method begins searching from this filter.

### -param riid [in]

Interface identifier (IID) of the interface to locate.

### -param ppint [out]

Address of a variable that receives the interface pointer. Be sure to release the retrieved interface pointer when you are done with the interface.

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
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
No such interface supported.

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

In a capture graph, various filters and pins might expose interfaces for setting properties such as compression parameters (<a href="/windows/desktop/api/strmif/nn-strmif-iamvideocompression">IAMVideoCompression</a>) or stream formats (<a href="/windows/desktop/api/strmif/nn-strmif-iamstreamconfig">IAMStreamConfig</a>). Depending on the capture device, other useful interfaces might include <a href="/windows/desktop/api/strmif/nn-strmif-iamcrossbar">IAMCrossbar</a>, which routes analog signals, or <a href="/windows/desktop/api/strmif/nn-strmif-iamtvtuner">IAMTVTuner</a>, which controls a TV tuner device. You can use this method to find an interface, without writing special code that traverses the graph.

<div class="alert"><b>Important</b>  Do not call this method to obtain an <a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow</a> interface pointer. Always query the filter graph manager for this interface. Otherwise, the filter graph manager will not respond correctly to changes in screen resolution and other events.</div>
<div> </div>
If the <i>pCategory</i> parameter is <b>NULL</b>, this method searches the entire graph for the requested interface. Starting from the filter specified by the <i>pf</i> parameter, it queries the following objects in the graph.

<ul>
<li>The filter</li>
<li>The filter's pins</li>
<li>All the downstream filters, including their pins</li>
<li>All the upstream filters, including their pins</li>
</ul>
You can restrict the search by setting the <i>pCategory</i> and <i>pType</i> parameters, as follows:

<ul>
<li>If <i>pCategory</i> equals &amp;LOOK_UPSTREAM_ONLY, the search starts from the filter's input pins and continues upstream. It does not include the filter or anything downstream from the filter. The <i>pType</i> parameter is ignored.</li>
<li>If <i>pCategory</i> equals &amp;LOOK_DOWNSTREAM_ONLY, the search starts from the filter's output pins and continues downstream. It does not include the filter or anything upstream from the filter. The <i>pType</i> parameter is ignored.</li>
<li>If <i>pCategory</i> specifies a pin category, the downstream portion of the search is restricted to output pins on the filter that match both the pin category and the media type given in the <i>pType</i> parameter. In this case, the method also searches the filter and everything upstream from the filter.</li>
</ul>
In addition, if <i>pCategory</i> is non-<b>NULL</b>, the method may add certain Windows Driver Model (WDM) filters upstream from filter specified in <i>pf</i>. See the remarks under "Supporting Filters" in this section for more information.

Pin categories are useful for finding pin interfaces on capture filters. For example, a capture filter might have separate pins for capture and preview. If you specify a pin category, you should also specify the media type, to make certain the method selects the correct filter and pin.

Some video capture filters have a video port pin (PIN_CATEGORY_VIDEOPORT) instead of a preview pin. If you specify PIN_CATEGORY_PREVIEW and MEDIATYPE_Video, the method treats any video port pins as preview pins. Your application does not have to test for this possibility.

<b>Supporting Filters</b>. If a capture device uses a Windows Driver Model (WDM) driver, the graph may require certain filters upstream from the <a href="/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture</a> filter, such as a <a href="/windows/desktop/DirectShow/tv-tuner-filter">TV Tuner</a> filter or an <a href="/windows/desktop/DirectShow/analog-video-crossbar-filter">Analog Video Crossbar</a> filter. If the <i>pCategory</i> parameter does not equal <b>NULL</b>, this method automatically inserts any required WDM filters into the graph. To do so, it queries the input pins on the capture filter to determine what mediums they support, and connects them to matching filters. If the <i>pCategory</i> parameter is <b>NULL</b>, the method does not add the upstream filters.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icapturegraphbuilder2">ICaptureGraphBuilder2 Interface</a>