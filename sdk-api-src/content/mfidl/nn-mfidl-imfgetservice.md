---
UID: NN:mfidl.IMFGetService
title: IMFGetService (mfidl.h)
description: Queries an object for a specified service interface. (IMFGetService)
helpviewer_keywords: ["102a1dff-8419-4f86-a145-53ce3d0123f5","IMFGetService","IMFGetService interface [Media Foundation]","IMFGetService interface [Media Foundation]","described","mf.imfgetservice","mfidl/IMFGetService"]
old-location: mf\imfgetservice.htm
tech.root: mf
ms.assetid: 102a1dff-8419-4f86-a145-53ce3d0123f5
ms.date: 12/05/2018
ms.keywords: 102a1dff-8419-4f86-a145-53ce3d0123f5, IMFGetService, IMFGetService interface [Media Foundation], IMFGetService interface [Media Foundation],described, mf.imfgetservice, mfidl/IMFGetService
req.header: mfidl.h
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
 - IMFGetService
 - mfidl/IMFGetService
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
 - IMFGetService
---

# IMFGetService interface


## -description

Queries an object for a specified service interface.

## -inheritance

The <b>IMFGetService</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFGetService</b> also has these types of members:

## -remarks

A service is an interface that is exposed by one object but might be implemented by another object. The <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">GetService</a> method is equivalent to <b>QueryInterface</b>, with the following difference: when <b>QueryInterface</b> retrieves a pointer to an interface, it is guaranteed that you can query the returned interface and get back the original interface. The <b>GetService</b> method does not make this guarantee, because the retrieved interface might be implemented by a separate object.

The <a href="/windows/desktop/api/mfidl/nf-mfidl-mfgetservice">MFGetService</a> function is a helper function that queries an object for <b>IMFGetService</b> and calls the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">GetService</a> method.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/service-interfaces">Service Interfaces</a>
