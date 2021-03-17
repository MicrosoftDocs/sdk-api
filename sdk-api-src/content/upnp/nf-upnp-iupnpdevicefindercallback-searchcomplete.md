---
UID: NF:upnp.IUPnPDeviceFinderCallback.SearchComplete
title: IUPnPDeviceFinderCallback::SearchComplete (upnp.h)
description: The SearchComplete method is invoked by the UPnP framework to notify the application that the initial search for network devices has been completed.
helpviewer_keywords: ["IUPnPDeviceFinderCallback interface [UPnP APIs]","SearchComplete method","IUPnPDeviceFinderCallback.SearchComplete","IUPnPDeviceFinderCallback::SearchComplete","SearchComplete","SearchComplete method [UPnP APIs]","SearchComplete method [UPnP APIs]","IUPnPDeviceFinderCallback interface","_upnp_iupnpdevicefindercallback_searchcomplete","upnp.iupnpdevicefindercallback_searchcomplete","upnp/IUPnPDeviceFinderCallback::SearchComplete"]
old-location: upnp\iupnpdevicefindercallback_searchcomplete.htm
tech.root: upnp
ms.assetid: 6fcce487-1cfb-47ec-9ea1-7df04985d506
ms.date: 12/05/2018
ms.keywords: IUPnPDeviceFinderCallback interface [UPnP APIs],SearchComplete method, IUPnPDeviceFinderCallback.SearchComplete, IUPnPDeviceFinderCallback::SearchComplete, SearchComplete, SearchComplete method [UPnP APIs], SearchComplete method [UPnP APIs],IUPnPDeviceFinderCallback interface, _upnp_iupnpdevicefindercallback_searchcomplete, upnp.iupnpdevicefindercallback_searchcomplete, upnp/IUPnPDeviceFinderCallback::SearchComplete
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Upnp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPDeviceFinderCallback::SearchComplete
 - upnp/IUPnPDeviceFinderCallback::SearchComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDeviceFinderCallback.SearchComplete
---

# IUPnPDeviceFinderCallback::SearchComplete


## -description

The 
<b>SearchComplete</b> method is invoked by the UPnP framework to notify the application that the initial search for network devices has been completed.

This method is invoked when the UPnP framework has finished sending <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefindercallback-deviceadded">IUPnPDeviceFinderCallback::DeviceAdded</a> or <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinderaddcallbackwithinterface-deviceaddedwithinterface">IUPnPDeviceFinderAddCallbackWithInterface::DeviceAddedWithInterface</a> callbacks for all devices that were present on the network at the time the search was started. These callbacks reflect the state of the network at the time the search was started.

## -parameters

### -param lFindData [in]

Specifies the search for which the UPnP framework is returning results. The value of <i>lFindData</i> is the value returned to the caller by 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-createasyncfind">IUPnPDeviceFinder::CreateAsyncFind</a>.

## -returns

The application should return S_OK.

## -remarks

This method simply provides information. It does not indicate that the asynchronous search has ended, but rather that the initial probe has completed. The asynchronous search continues to report devices being added to and removed from the network until the application calls 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-cancelasyncfind">IUPnPDeviceFinder::CancelAsyncFind</a>.

The initial search can take a long time to complete. The <b>SearchComplete</b> callback is invoked when the description document for the last device found (that is, the last device found to be present on the network at the time the search was started) has either been loaded or has failed to load.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinder">IUPnPDeviceFinder</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-createasyncfind">IUPnPDeviceFinder::CreateAsyncFind</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefindercallback">IUPnPDeviceFinderCallback</a>