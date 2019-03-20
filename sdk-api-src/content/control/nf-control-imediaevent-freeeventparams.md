---
UID: NF:control.IMediaEvent.FreeEventParams
title: IMediaEvent::FreeEventParams (control.h)
author: windows-sdk-content
description: The FreeEventParams method frees resources associated with the parameters of an event.
old-location: dshow\imediaevent_freeeventparams.htm
tech.root: DirectShow
ms.assetid: d98f37a4-3482-4cf7-bede-c7e7be70652a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FreeEventParams, FreeEventParams method [DirectShow], FreeEventParams method [DirectShow],IMediaEvent interface, FreeEventParams method [DirectShow],IMediaEventEx interface, IMediaEvent interface [DirectShow],FreeEventParams method, IMediaEvent.FreeEventParams, IMediaEvent::FreeEventParams, IMediaEventEx interface [DirectShow],FreeEventParams method, IMediaEventEx::FreeEventParams, IMediaEventFreeEventParams, control/IMediaEvent::FreeEventParams, control/IMediaEventEx::FreeEventParams, dshow.imediaevent_freeeventparams
ms.topic: method
req.header: control.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaEvent.FreeEventParams
 - IMediaEventEx.FreeEventParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaEvent::FreeEventParams


## -description



The <code>FreeEventParams</code> method frees resources associated with the parameters of an event.




## -parameters




### -param lEvCode [in]

Event code.


### -param lParam1 [in]

First event parameter.


### -param lParam2 [in]

Second event parameter.


## -returns



Returns S_OK.




## -remarks



After you call the <a href="https://msdn.microsoft.com/en-us/library/Dd406907(v=VS.85).aspx">IMediaEvent::GetEvent</a> method to retrieve an event notification, you must call <code>FreeEventParams</code>. This method frees any resources that were allocated for the event parameters. Pass in the same variables used for the <b>GetEvent</b> call.


#### Examples


```cpp

hr = pEvent->GetEvent(&evCode, &param1, &param2, 0);
// Handle the event (not shown). 
hr = pEvent->FreeEventParams(evCode, param1, param2);

```





## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406896(v=VS.85).aspx">IMediaEvent Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406897(v=VS.85).aspx">IMediaEventEx</a>
 

 

