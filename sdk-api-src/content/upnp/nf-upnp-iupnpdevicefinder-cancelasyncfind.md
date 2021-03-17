---
UID: NF:upnp.IUPnPDeviceFinder.CancelAsyncFind
title: IUPnPDeviceFinder::CancelAsyncFind (upnp.h)
description: The CancelAsyncFind method cancels an asynchronous search.
helpviewer_keywords: ["CancelAsyncFind","CancelAsyncFind method [UPnP APIs]","CancelAsyncFind method [UPnP APIs]","IUPnPDeviceFinder interface","IUPnPDeviceFinder interface [UPnP APIs]","CancelAsyncFind method","IUPnPDeviceFinder.CancelAsyncFind","IUPnPDeviceFinder::CancelAsyncFind","_upnp_iupnpdevicefinder_cancelasyncfind","upnp.iupnpdevicefinder_cancelasyncfind","upnp/IUPnPDeviceFinder::CancelAsyncFind"]
old-location: upnp\iupnpdevicefinder_cancelasyncfind.htm
tech.root: upnp
ms.assetid: d64db4fe-0b0a-430f-b198-dd49ef40b52e
ms.date: 12/05/2018
ms.keywords: CancelAsyncFind, CancelAsyncFind method [UPnP APIs], CancelAsyncFind method [UPnP APIs],IUPnPDeviceFinder interface, IUPnPDeviceFinder interface [UPnP APIs],CancelAsyncFind method, IUPnPDeviceFinder.CancelAsyncFind, IUPnPDeviceFinder::CancelAsyncFind, _upnp_iupnpdevicefinder_cancelasyncfind, upnp.iupnpdevicefinder_cancelasyncfind, upnp/IUPnPDeviceFinder::CancelAsyncFind
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
 - IUPnPDeviceFinder::CancelAsyncFind
 - upnp/IUPnPDeviceFinder::CancelAsyncFind
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
 - IUPnPDeviceFinder.CancelAsyncFind
---

# IUPnPDeviceFinder::CancelAsyncFind


## -description

The 
<b>CancelAsyncFind</b> method cancels an asynchronous search.

## -parameters

### -param lFindData [in]

Specifies the search to cancel. The value of <i>lFindData</i> is the value returned by a previous call to 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-createasyncfind">IUPnPDeviceFinder::CreateAsyncFind</a>.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

Applications can keep asynchronous searches running until the application exits. Always cancel outstanding operations when exiting an application.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinder">IUPnPDeviceFinder</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-createasyncfind">IUPnPDeviceFinder::CreateAsyncFind</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-startasyncfind">IUPnPDeviceFinder::StartAsyncFind</a>