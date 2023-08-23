---
UID: NF:strmif.IGraphConfig.Reconfigure
title: IGraphConfig::Reconfigure (strmif.h)
description: The Reconfigure method locks the filter graph and calls a callback function in the application or filter to perform a dynamic reconfiguration.
helpviewer_keywords: ["IGraphConfig interface [DirectShow]","Reconfigure method","IGraphConfig.Reconfigure","IGraphConfig::Reconfigure","IGraphConfigReconfigure","Reconfigure","Reconfigure method [DirectShow]","Reconfigure method [DirectShow]","IGraphConfig interface","dshow.igraphconfig_reconfigure","strmif/IGraphConfig::Reconfigure"]
old-location: dshow\igraphconfig_reconfigure.htm
tech.root: dshow
ms.assetid: 924087c0-e3ad-437b-96e5-de39bbce2ea7
ms.date: 4/26/2023
ms.keywords: IGraphConfig interface [DirectShow],Reconfigure method, IGraphConfig.Reconfigure, IGraphConfig::Reconfigure, IGraphConfigReconfigure, Reconfigure, Reconfigure method [DirectShow], Reconfigure method [DirectShow],IGraphConfig interface, dshow.igraphconfig_reconfigure, strmif/IGraphConfig::Reconfigure
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
 - IGraphConfig::Reconfigure
 - strmif/IGraphConfig::Reconfigure
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
 - IGraphConfig.Reconfigure
---

# IGraphConfig::Reconfigure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Reconfigure</code> method locks the filter graph and calls a callback function in the application or filter to perform a dynamic reconfiguration.

## -parameters

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-igraphconfigcallback">IGraphConfigCallback</a> callback interface on the application or filter.

### -param pvContext [in]

Pointer to a variable of type <b>PVOID</b> that is passed to the callback routine.

### -param dwFlags [in]

Application-defined flags that are passed to the callback routine.

### -param hAbortEvent [in]

Handle to an event. If the caller is a filter calling on one of its data processing threads, this parameter should be a handle to an event that will be signaled when the filter is put into a stopped state. Otherwise, this parameter can be <b>NULL</b>. For more information, see Remarks.

## -returns

Returns S_OK if successful, or an error code otherwise. Possible errors include VFW_E_WRONG_STATE, if the method could not obtain a lock on the filter graph; whatever <b>HRESULT</b> was returned by the callback routine; or an error code indicating that the graph could not put the filters into a running state.

## -remarks

This method is provided so that an application or filter can implement specialized dynamic graph building. In most cases, however, the <a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-reconnect">IGraphConfig::Reconnect</a> method is adequate, and should be preferred because it handles most of the implementation details.

Before calling this method, block any streams as needed and push the data through the graph (see <a href="/windows/desktop/api/strmif/nf-strmif-ipinflowcontrol-block">IPinFlowControl::Block</a> and <a href="/windows/desktop/api/strmif/nf-strmif-igraphconfig-pushthroughdata">IGraphConfig::PushThroughData</a>). If the callback method succeeds, <code>IGraphConfig::Reconfigure</code> attempts to put all the filters into a running state. (The caller must then unblock the data flow.) Otherwise, it returns whatever error code the callback method returned.

If a filter calls this method on one of its own data processing threads, it creates the potential for a deadlock. The method obtains a lock on the filter graph, which can block the filter from stopping on receiving a call to <a href="/windows/desktop/api/strmif/nf-strmif-imediafilter-stop">IMediaFilter::Stop</a>. To prevent this situation, the method takes a handle to an event object provided by filter. The filter should signal the event if it receives a call to its <b>Stop</b> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig Interface</a>