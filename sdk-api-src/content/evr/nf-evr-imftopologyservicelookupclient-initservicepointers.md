---
UID: NF:evr.IMFTopologyServiceLookupClient.InitServicePointers
title: IMFTopologyServiceLookupClient::InitServicePointers (evr.h)
description: Signals the mixer or presenter to query the enhanced video renderer (EVR) for interface pointers.
helpviewer_keywords: ["IMFTopologyServiceLookupClient interface [Media Foundation]","InitServicePointers method","IMFTopologyServiceLookupClient.InitServicePointers","IMFTopologyServiceLookupClient::InitServicePointers","InitServicePointers","InitServicePointers method [Media Foundation]","InitServicePointers method [Media Foundation]","IMFTopologyServiceLookupClient interface","b89f5a47-154c-455a-b5a2-db55e4972b21","evr/IMFTopologyServiceLookupClient::InitServicePointers","mf.imftopologyservicelookupclient_initservicepointers"]
old-location: mf\imftopologyservicelookupclient_initservicepointers.htm
tech.root: mfarchive
ms.assetid: b89f5a47-154c-455a-b5a2-db55e4972b21
ms.date: 12/05/2018
ms.keywords: IMFTopologyServiceLookupClient interface [Media Foundation],InitServicePointers method, IMFTopologyServiceLookupClient.InitServicePointers, IMFTopologyServiceLookupClient::InitServicePointers, InitServicePointers, InitServicePointers method [Media Foundation], InitServicePointers method [Media Foundation],IMFTopologyServiceLookupClient interface, b89f5a47-154c-455a-b5a2-db55e4972b21, evr/IMFTopologyServiceLookupClient::InitServicePointers, mf.imftopologyservicelookupclient_initservicepointers
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
 - IMFTopologyServiceLookupClient::InitServicePointers
 - evr/IMFTopologyServiceLookupClient::InitServicePointers
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
 - IMFTopologyServiceLookupClient.InitServicePointers
archived: true
---

# IMFTopologyServiceLookupClient::InitServicePointers


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Signals the mixer or presenter to query the enhanced video renderer (EVR) for interface pointers.

## -parameters

### -param pLookup [in]

Pointer to the <a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookup">IMFTopologyServiceLookup</a> interface. To query the EVR for an interface, call <a href="/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice">IMFTopologyServiceLookup::LookupService</a>.

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
</table>

## -remarks

The <a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookup">IMFTopologyServiceLookup</a> pointer is guaranteed to be valid only during the call to <b>InitServicePointers</b>. The mixer or presenter should not store a pointer to this interface after the method returns.

When the EVR calls <a href="/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers">IMFTopologyServiceLookupClient::ReleaseServicePointers</a>, the mixer or presenter should release any pointers it obtained from the EVR.

## -see-also

<a href="/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient">IMFTopologyServiceLookupClient</a>