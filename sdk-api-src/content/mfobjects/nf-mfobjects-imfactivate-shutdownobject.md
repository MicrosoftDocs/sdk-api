---
UID: NF:mfobjects.IMFActivate.ShutdownObject
title: IMFActivate::ShutdownObject (mfobjects.h)
description: Shuts down the created object.
helpviewer_keywords: ["1f88ff31-5a91-4838-bfce-673a5a85c766","IMFActivate interface [Media Foundation]","ShutdownObject method","IMFActivate.ShutdownObject","IMFActivate::ShutdownObject","ShutdownObject","ShutdownObject method [Media Foundation]","ShutdownObject method [Media Foundation]","IMFActivate interface","mf.imfactivate_shutdownobject","mfobjects/IMFActivate::ShutdownObject"]
old-location: mf\imfactivate_shutdownobject.htm
tech.root: mf
ms.assetid: 1f88ff31-5a91-4838-bfce-673a5a85c766
ms.date: 12/05/2018
ms.keywords: 1f88ff31-5a91-4838-bfce-673a5a85c766, IMFActivate interface [Media Foundation],ShutdownObject method, IMFActivate.ShutdownObject, IMFActivate::ShutdownObject, ShutdownObject, ShutdownObject method [Media Foundation], ShutdownObject method [Media Foundation],IMFActivate interface, mf.imfactivate_shutdownobject, mfobjects/IMFActivate::ShutdownObject
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFActivate::ShutdownObject
 - mfobjects/IMFActivate::ShutdownObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFActivate.ShutdownObject
---

# IMFActivate::ShutdownObject


## -description

Shuts down the created object.



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

If you create an object by calling <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a>, call <b>ShutdownObject</b> when you are done using the object.

The component that calls <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">ActivateObject</a>—not the component that creates the activation object—is responsible for calling <b>ShutdownObject</b>. For example, in a typical playback application, the application creates activation objects for the media sinks, but the Media Session calls <b>ActivateObject</b>. Therefore the Media Session, not the application, calls <b>ShutdownObject</b>.

After <b>ShutdownObject</b> is called, the activation object releases all of its internal references to the created object. If you call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">ActivateObject</a> again, the activation object will create a new instance of the other object.

## -see-also

<a href="/windows/desktop/medfound/activation-objects">Activation Objects</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a>
