---
UID: NF:evr.IMFTopologyServiceLookupClient.ReleaseServicePointers
title: IMFTopologyServiceLookupClient::ReleaseServicePointers (evr.h)
description: Signals the object to release the interface pointers obtained from the enhanced video renderer (EVR).
helpviewer_keywords: ["03ed29b4-89c1-4702-a23f-d013eeef5d44","IMFTopologyServiceLookupClient interface [Media Foundation]","ReleaseServicePointers method","IMFTopologyServiceLookupClient.ReleaseServicePointers","IMFTopologyServiceLookupClient::ReleaseServicePointers","ReleaseServicePointers","ReleaseServicePointers method [Media Foundation]","ReleaseServicePointers method [Media Foundation]","IMFTopologyServiceLookupClient interface","evr/IMFTopologyServiceLookupClient::ReleaseServicePointers","mf.imftopologyservicelookupclient_releaseservicepointers"]
old-location: mf\imftopologyservicelookupclient_releaseservicepointers.htm
tech.root: mfarchive
ms.assetid: 03ed29b4-89c1-4702-a23f-d013eeef5d44
ms.date: 12/05/2018
ms.keywords: 03ed29b4-89c1-4702-a23f-d013eeef5d44, IMFTopologyServiceLookupClient interface [Media Foundation],ReleaseServicePointers method, IMFTopologyServiceLookupClient.ReleaseServicePointers, IMFTopologyServiceLookupClient::ReleaseServicePointers, ReleaseServicePointers, ReleaseServicePointers method [Media Foundation], ReleaseServicePointers method [Media Foundation],IMFTopologyServiceLookupClient interface, evr/IMFTopologyServiceLookupClient::ReleaseServicePointers, mf.imftopologyservicelookupclient_releaseservicepointers
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
 - IMFTopologyServiceLookupClient::ReleaseServicePointers
 - evr/IMFTopologyServiceLookupClient::ReleaseServicePointers
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
 - IMFTopologyServiceLookupClient.ReleaseServicePointers
archived: true
---

# IMFTopologyServiceLookupClient::ReleaseServicePointers


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Signals the object to release the interface pointers obtained from the enhanced video renderer (EVR).



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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

After this method is called, any interface pointers obtained during the previous call to <a href="/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers">IMFTopologyServiceLookupClient::InitServicePointers</a> are no longer valid. The object must release them.

## -see-also

<a href="/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient">IMFTopologyServiceLookupClient</a>
