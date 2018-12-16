---
UID: NF:mfobjects.IMFActivate.ActivateObject
title: IMFActivate::ActivateObject
author: windows-sdk-content
description: Creates the object associated with this activation object.
old-location: mf\imfactivate_activateobject.htm
tech.root: medfound
ms.assetid: 120b8070-6732-450d-8334-b3910f7bb4d2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 120b8070-6732-450d-8334-b3910f7bb4d2, ActivateObject, ActivateObject method [Media Foundation], ActivateObject method [Media Foundation],IMFActivate interface, IMFActivate interface [Media Foundation],ActivateObject method, IMFActivate.ActivateObject, IMFActivate::ActivateObject, mf.imfactivate_activateobject, mfobjects/IMFActivate::ActivateObject
ms.topic: method
req.header: mfobjects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFActivate.ActivateObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFActivate::ActivateObject


## -description


Creates the object associated with this activation object.
        


## -parameters




### -param riid [in]

Interface identifier (IID) of the requested interface.
          


### -param ppv [out]

Receives a pointer to the requested interface. The caller must release the interface.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Some Microsoft Media Foundation objects must be shut down before being released. If so, the caller is responsible for shutting down the object that is returned in <i>ppv</i>. To shut down the object, do one of the following:

<ul>
<li>Call <a href="https://msdn.microsoft.com/1f88ff31-5a91-4838-bfce-673a5a85c766">IMFActivate::ShutdownObject</a> on the activation object, or</li>
<li>Call the object-specific shutdown method. This method will depend on the type of object. Possibilities include:<ul>
<li>Media sources: Call <a href="https://msdn.microsoft.com/c7f890a8-74bd-4418-bb02-a3fee62dec6d">IMFMediaSource::Shutdown</a>.</li>
<li>Media sinks: Call <a href="https://msdn.microsoft.com/acda4e37-2dd0-4322-90fc-8f48d6842054">IMFMediaSink::Shutdown</a>.</li>
<li>Any object that supports the <a href="https://msdn.microsoft.com/c3052658-51bb-401b-8db9-3428868899d6">IMFShutdown</a> interface: Call <a href="https://msdn.microsoft.com/9e7824d2-0f76-4c4c-98c5-ba51cd297de7">IMFShutdown::Shutdown</a>.</li>
</ul>
</li>
</ul>
The <a href="https://msdn.microsoft.com/1f88ff31-5a91-4838-bfce-673a5a85c766">IMFActivate::ShutdownObject</a> method is generic to all object types. If the object does not require a shutdown method, <b>ShutdownObject</b> succeeds and has no effect. If you do not know the specific shutdown method for the object (or do not know the object type), call <b>IMFActivate::ShutdownObject</b>.

After the first call to <b>ActivateObject</b>, subsequent calls return a pointer to the same instance, until the client calls either <a href="https://msdn.microsoft.com/1f88ff31-5a91-4838-bfce-673a5a85c766">ShutdownObject</a> or <a href="https://msdn.microsoft.com/15216c57-f85d-4087-ad52-d35059647828">IMFActivate::DetachObject</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/767d5f1c-2b8d-43b6-916b-035129e93204">Activation Objects</a>



<a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a>
 

 

