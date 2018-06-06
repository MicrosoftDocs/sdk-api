---
UID: NF:upnp.IUPnPDeviceFinder.CancelAsyncFind
title: IUPnPDeviceFinder::CancelAsyncFind
author: windows-sdk-content
description: The CancelAsyncFind method cancels an asynchronous search.
old-location: upnp\iupnpdevicefinder_cancelasyncfind.htm
old-project: UPnP
ms.assetid: d64db4fe-0b0a-430f-b198-dd49ef40b52e
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: CancelAsyncFind, CancelAsyncFind method [UPnP APIs], CancelAsyncFind method [UPnP APIs],IUPnPDeviceFinder interface, IUPnPDeviceFinder interface [UPnP APIs],CancelAsyncFind method, IUPnPDeviceFinder.CancelAsyncFind, IUPnPDeviceFinder::CancelAsyncFind, _upnp_iupnpdevicefinder_cancelasyncfind, upnp.iupnpdevicefinder_cancelasyncfind, upnp/IUPnPDeviceFinder::CancelAsyncFind
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDeviceFinder.CancelAsyncFind
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDeviceFinder::CancelAsyncFind


## -description


The 
<b>CancelAsyncFind</b> method cancels an asynchronous search.


## -parameters




### -param lFindData [in]

Specifies the search to cancel. The value of <i>lFindData</i> is the value returned by a previous call to 
<a href="https://msdn.microsoft.com/4461b53f-b630-4b4a-bc68-0cc48ef70594">IUPnPDeviceFinder::CreateAsyncFind</a>.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



Applications can keep asynchronous searches running until the application exits. Always cancel outstanding operations when exiting an application.




## -see-also




<a href="https://msdn.microsoft.com/a4697038-8abc-42f2-9381-702fc82af90b">IUPnPDeviceFinder</a>



<a href="https://msdn.microsoft.com/4461b53f-b630-4b4a-bc68-0cc48ef70594">IUPnPDeviceFinder::CreateAsyncFind</a>



<a href="https://msdn.microsoft.com/3189ea47-8cb3-4b95-b88d-7ff72b776e56">IUPnPDeviceFinder::StartAsyncFind</a>
 

 

