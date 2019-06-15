---
UID: NF:mfobjects.IMFActivate.ActivateObject
title: IMFActivate::ActivateObject (mfobjects.h)
author: windows-sdk-content
description: Creates the object associated with this activation object.
old-location: mf\imfactivate_activateobject.htm
tech.root: medfound
ms.assetid: 120b8070-6732-450d-8334-b3910f7bb4d2
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
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
<li>Call <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject">IMFActivate::ShutdownObject</a> on the activation object, or</li>
<li>Call the object-specific shutdown method. This method will depend on the type of object. Possibilities include:<ul>
<li>Media sources: Call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown">IMFMediaSource::Shutdown</a>.</li>
<li>Media sinks: Call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown">IMFMediaSink::Shutdown</a>.</li>
<li>Any object that supports the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfshutdown">IMFShutdown</a> interface: Call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown">IMFShutdown::Shutdown</a>.</li>
</ul>
</li>
</ul>
The <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject">IMFActivate::ShutdownObject</a> method is generic to all object types. If the object does not require a shutdown method, <b>ShutdownObject</b> succeeds and has no effect. If you do not know the specific shutdown method for the object (or do not know the object type), call <b>IMFActivate::ShutdownObject</b>.

After the first call to <b>ActivateObject</b>, subsequent calls return a pointer to the same instance, until the client calls either <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject">ShutdownObject</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-detachobject">IMFActivate::DetachObject</a>.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/activation-objects">Activation Objects</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a>
 

 

