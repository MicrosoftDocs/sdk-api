---
UID: NN:mfobjects.IMFActivate
title: IMFActivate (mfobjects.h)
description: Enables the application to defer the creation of an object.
helpviewer_keywords: ["IMFActivate","IMFActivate interface [Media Foundation]","IMFActivate interface [Media Foundation]","described","c0936e3c-3cd1-4c1e-a336-2dee7d943963","mf.imfactivate","mfobjects/IMFActivate"]
old-location: mf\imfactivate.htm
tech.root: mf
ms.assetid: c0936e3c-3cd1-4c1e-a336-2dee7d943963
ms.date: 12/05/2018
ms.keywords: IMFActivate, IMFActivate interface [Media Foundation], IMFActivate interface [Media Foundation],described, c0936e3c-3cd1-4c1e-a336-2dee7d943963, mf.imfactivate, mfobjects/IMFActivate
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
 - IMFActivate
 - mfobjects/IMFActivate
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
 - IMFActivate
---

# IMFActivate interface


## -description

Enables the application to defer the creation of an object. This interface is exposed by activation objects.

## -inheritance

The <b>IMFActivate</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFActivate</b> also has these types of members:

## -remarks

Typically, the application calls some function that returns an <b>IMFActivate</b> pointer and then passes that pointer to another component. The other component calls <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">ActivateObject</a> at a later time to create the object. In the protected media path (PMP), the <b>IMFActivate</b> pointer might be marshaled to the protected process, so that the object can be created in that process.

## -see-also

<a href="/windows/desktop/medfound/activation-objects">Activation Objects</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
