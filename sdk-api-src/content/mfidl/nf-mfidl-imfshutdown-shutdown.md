---
UID: NF:mfidl.IMFShutdown.Shutdown
title: IMFShutdown::Shutdown (mfidl.h)
description: Shuts down a Media Foundation object and releases all resources associated with the object. (IMFShutdown.Shutdown)
helpviewer_keywords: ["9e7824d2-0f76-4c4c-98c5-ba51cd297de7","IMFShutdown interface [Media Foundation]","Shutdown method","IMFShutdown.Shutdown","IMFShutdown::Shutdown","Shutdown","Shutdown method [Media Foundation]","Shutdown method [Media Foundation]","IMFShutdown interface","mf.imfshutdown_shutdown","mfidl/IMFShutdown::Shutdown"]
old-location: mf\imfshutdown_shutdown.htm
tech.root: mf
ms.assetid: 9e7824d2-0f76-4c4c-98c5-ba51cd297de7
ms.date: 12/05/2018
ms.keywords: 9e7824d2-0f76-4c4c-98c5-ba51cd297de7, IMFShutdown interface [Media Foundation],Shutdown method, IMFShutdown.Shutdown, IMFShutdown::Shutdown, Shutdown, Shutdown method [Media Foundation], Shutdown method [Media Foundation],IMFShutdown interface, mf.imfshutdown_shutdown, mfidl/IMFShutdown::Shutdown
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
 - IMFShutdown::Shutdown
 - mfidl/IMFShutdown::Shutdown
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
 - IMFShutdown.Shutdown
---

# IMFShutdown::Shutdown


## -description

Shuts down a Media Foundation object and releases all resources associated with the object.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/desktop/api/mfidl/nf-mfidl-mfshutdownobject">MFShutdownObject</a>  helper function is equivalent to calling this method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfshutdown">IMFShutdown</a>



<a href="/windows/desktop/api/mfidl/nf-mfidl-mfshutdownobject">MFShutdownObject</a>
