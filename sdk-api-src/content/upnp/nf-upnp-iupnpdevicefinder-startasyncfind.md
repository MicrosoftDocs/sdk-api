---
UID: NF:upnp.IUPnPDeviceFinder.StartAsyncFind
title: IUPnPDeviceFinder::StartAsyncFind (upnp.h)
author: windows-sdk-content
description: The StartAsyncFind method starts an asynchronous search operation.
old-location: upnp\iupnpdevicefinder_startasyncfind.htm
tech.root: upnp
ms.assetid: 3189ea47-8cb3-4b95-b88d-7ff72b776e56
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPDeviceFinder interface [UPnP APIs],StartAsyncFind method, IUPnPDeviceFinder.StartAsyncFind, IUPnPDeviceFinder::StartAsyncFind, StartAsyncFind, StartAsyncFind method [UPnP APIs], StartAsyncFind method [UPnP APIs],IUPnPDeviceFinder interface, _upnp_iupnpdevicefinder_startasyncfind, upnp.iupnpdevicefinder_startasyncfind, upnp/IUPnPDeviceFinder::StartAsyncFind
ms.topic: method
f1_keywords: ["upnp/IUPnPDeviceFinder.StartAsyncFind"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDeviceFinder.StartAsyncFind
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPDeviceFinder::StartAsyncFind


## -description


The 
<b>StartAsyncFind</b> method starts an asynchronous search operation.


## -parameters




### -param lFindData [in]

Specifies the search to start. The value of <i>lFindData</i> is the value returned by a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-createasyncfind">IUPnPDeviceFinder::CreateAsyncFind</a>.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



You can have more than one 
<b>StartAsyncFind</b> operation running at the same time; starting another 
<b>StartAsyncFind</b> does not cancel a previous 
<b>StartAsyncFind</b> operation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinder">IUPnPDeviceFinder</a>



<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-cancelasyncfind">IUPnPDeviceFinder::CancelAsyncFind</a>
 

 

