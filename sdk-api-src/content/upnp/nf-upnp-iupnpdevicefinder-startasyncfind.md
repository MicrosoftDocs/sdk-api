---
UID: NF:upnp.IUPnPDeviceFinder.StartAsyncFind
title: IUPnPDeviceFinder::StartAsyncFind
author: windows-sdk-content
description: The StartAsyncFind method starts an asynchronous search operation.
old-location: upnp\iupnpdevicefinder_startasyncfind.htm
tech.root: upnp
ms.assetid: 3189ea47-8cb3-4b95-b88d-7ff72b776e56
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IUPnPDeviceFinder interface [UPnP APIs],StartAsyncFind method, IUPnPDeviceFinder.StartAsyncFind, IUPnPDeviceFinder::StartAsyncFind, StartAsyncFind, StartAsyncFind method [UPnP APIs], StartAsyncFind method [UPnP APIs],IUPnPDeviceFinder interface, _upnp_iupnpdevicefinder_startasyncfind, upnp.iupnpdevicefinder_startasyncfind, upnp/IUPnPDeviceFinder::StartAsyncFind
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IUPnPDeviceFinder::StartAsyncFind


## -description


The 
<b>StartAsyncFind</b> method starts an asynchronous search operation.


## -parameters




### -param lFindData [in]

Specifies the search to start. The value of <i>lFindData</i> is the value returned by a previous call to 
<a href="https://msdn.microsoft.com/4461b53f-b630-4b4a-bc68-0cc48ef70594">IUPnPDeviceFinder::CreateAsyncFind</a>.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



You can have more than one 
<b>StartAsyncFind</b> operation running at the same time; starting another 
<b>StartAsyncFind</b> does not cancel a previous 
<b>StartAsyncFind</b> operation.




## -see-also




<a href="https://msdn.microsoft.com/a4697038-8abc-42f2-9381-702fc82af90b">IUPnPDeviceFinder</a>



<a href="https://msdn.microsoft.com/d64db4fe-0b0a-430f-b198-dd49ef40b52e">IUPnPDeviceFinder::CancelAsyncFind</a>
 

 

