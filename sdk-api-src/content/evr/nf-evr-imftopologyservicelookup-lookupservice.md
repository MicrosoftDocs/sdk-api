---
UID: NF:evr.IMFTopologyServiceLookup.LookupService
title: IMFTopologyServiceLookup::LookupService (evr.h)
description: Retrieves an interface from the enhanced video renderer (EVR), or from the video mixer or video presenter.
helpviewer_keywords: ["IMFTopologyServiceLookup interface [Media Foundation]","LookupService method","IMFTopologyServiceLookup.LookupService","IMFTopologyServiceLookup::LookupService","LookupService","LookupService method [Media Foundation]","LookupService method [Media Foundation]","IMFTopologyServiceLookup interface","ba0dbfdf-1bab-42ba-910f-04a3f37be955","evr/IMFTopologyServiceLookup::LookupService","mf.imftopologyservicelookup_lookupservice"]
old-location: mf\imftopologyservicelookup_lookupservice.htm
tech.root: mfarchive
ms.assetid: ba0dbfdf-1bab-42ba-910f-04a3f37be955
ms.date: 12/05/2018
ms.keywords: IMFTopologyServiceLookup interface [Media Foundation],LookupService method, IMFTopologyServiceLookup.LookupService, IMFTopologyServiceLookup::LookupService, LookupService, LookupService method [Media Foundation], LookupService method [Media Foundation],IMFTopologyServiceLookup interface, ba0dbfdf-1bab-42ba-910f-04a3f37be955, evr/IMFTopologyServiceLookup::LookupService, mf.imftopologyservicelookup_lookupservice
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFTopologyServiceLookup::LookupService
 - evr/IMFTopologyServiceLookup::LookupService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFTopologyServiceLookup.LookupService
archived: true
---

# IMFTopologyServiceLookup::LookupService


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Retrieves an interface from the enhanced video renderer (EVR), or from the video mixer or video presenter.

## -parameters

### -param Type [in]

Specifies the scope of the search. Currently this parameter is ignored. Use the value MF_SERVICE_LOOKUP_GLOBAL.

### -param dwIndex [in]

Reserved, must be zero.

### -param guidService [in]

Service GUID of the requested interface.

### -param riid [in]

Interface identifier of the requested interface.

### -param ppvObjects [out]

Array of interface pointers. If the method succeeds, each member of the array contains either a valid interface pointer or <b>NULL</b>. The caller must release the interface pointers when the EVR calls <a href="/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers">IMFTopologyServiceLookupClient::ReleaseServicePointers</a> (or earlier). If the method fails, every member of the array is <b>NULL</b>.

### -param pnObjects [in, out]

Pointer to a value that specifies the size of the <i>ppvObjects</i> array. The value must be at least 1. In the current implementation, there is no reason to specify an array size larger than one element. The value is not changed on output.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The requested interface is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOTACCEPTING</b></dt>
</dl>
</td>
<td width="60%">
The method was not called from inside the <a href="/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers">IMFTopologyServiceLookupClient::InitServicePointers</a> method. See Remarks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_SERVICE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the specified service GUID.

</td>
</tr>
</table>

## -remarks

This method can be called only from inside the <a href="/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers">IMFTopologyServiceLookupClient::InitServicePointers</a> method. At any other time, the method returns MF_E_NOTACCEPTING.

The presenter can use this method to query the EVR and the mixer. The mixer can use it to query the EVR and the presenter. Which objects are queried depends on the caller and the service GUID, as shown in the following table.

<table>
<tr>
<th>Caller</th>
<th>Service GUID</th>
<th>Objects queried</th>
</tr>
<tr>
<td>Presenter</td>
<td>MR_VIDEO_RENDER_SERVICE</td>
<td>EVR</td>
</tr>
<tr>
<td>Presenter</td>
<td>MR_VIDEO_MIXER_SERVICE</td>
<td>Mixer</td>
</tr>
<tr>
<td>Mixer</td>
<td>MR_VIDEO_RENDER_SERVICE</td>
<td>Presenter and EVR</td>
</tr>
</table>
 

The following interfaces are available from the EVR:

<ul>
<li>
<b>IMediaEventSink</b>. This interface is documented in the DirectShow SDK documentation.

</li>
<li>

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock">IMFClock</a> interface. This interface is available if the EVR has access to a clock (reference clock in DirectShow or presentation clock in Media Foundation). This interface might not be available. Presenter and mixers must be able to process data without a clock. If the <b>IMFClock</b> interface is available, you can also get these related interfaces:

<ul>
<li>

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftimer">IMFTimer</a>


</li>
<li>

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a> (Media Foundation EVR only)

</li>
</ul>
</li>
</ul>
The following interfaces are available from the mixer:

<ul>
<li>

<a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>


</li>
<li>

<a href="/windows/desktop/api/evr/nn-evr-imfvideodeviceid">IMFVideoDeviceID</a>


</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookup">IMFTopologyServiceLookup</a>