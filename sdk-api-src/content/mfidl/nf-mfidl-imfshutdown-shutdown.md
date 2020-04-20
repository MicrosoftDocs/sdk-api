---
UID: NF:mfidl.IMFShutdown.Shutdown
title: IMFShutdown::Shutdown (mfidl.h)
description: Shuts down a Media Foundation object and releases all resources associated with the object.helpviewer_keywords: ["9e7824d2-0f76-4c4c-98c5-ba51cd297de7","IMFShutdown interface [Media Foundation]","Shutdown method","IMFShutdown.Shutdown","IMFShutdown::Shutdown","Shutdown","Shutdown method [Media Foundation]","Shutdown method [Media Foundation]","IMFShutdown interface","mf.imfshutdown_shutdown","mfidl/IMFShutdown::Shutdown"]
old-location: mf\imfshutdown_shutdown.htm
tech.root: medfound
ms.assetid: 9e7824d2-0f76-4c4c-98c5-ba51cd297de7
ms.date: 12/05/2018
ms.keywords: 9e7824d2-0f76-4c4c-98c5-ba51cd297de7, IMFShutdown interface [Media Foundation],Shutdown method, IMFShutdown.Shutdown, IMFShutdown::Shutdown, Shutdown, Shutdown method [Media Foundation], Shutdown method [Media Foundation],IMFShutdown interface, mf.imfshutdown_shutdown, mfidl/IMFShutdown::Shutdown
f1_keywords:
- mfidl/IMFShutdown.Shutdown
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFShutdown::Shutdown


## -description


Shuts down a Media Foundation object and releases all resources associated with the object.
        


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfshutdownobject">MFShutdownObject</a>  helper function is equivalent to calling this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfshutdown">IMFShutdown</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfshutdownobject">MFShutdownObject</a>
 

 

