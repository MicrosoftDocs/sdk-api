---
UID: NF:objidl.ISurrogateService.Init
title: ISurrogateService::Init (objidl.h)
description: Initializes the process server.
helpviewer_keywords: ["ISurrogateService interface [COM]","Init method","ISurrogateService.Init","ISurrogateService::Init","Init","Init method [COM]","Init method [COM]","ISurrogateService interface","_com_isurrogateservice_init","com.isurrogateservice_init","objidl/ISurrogateService::Init"]
old-location: com\isurrogateservice_init.htm
tech.root: com
ms.assetid: ed2e628c-5c86-48fd-aa55-f532602247ea
ms.date: 12/05/2018
ms.keywords: ISurrogateService interface [COM],Init method, ISurrogateService.Init, ISurrogateService::Init, Init, Init method [COM], Init method [COM],ISurrogateService interface, _com_isurrogateservice_init, com.isurrogateservice_init, objidl/ISurrogateService::Init
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISurrogateService::Init
 - objidl/ISurrogateService::Init
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - ISurrogateService.Init
---

# ISurrogateService::Init


## -description

Initializes the process server.

## -parameters

### -param rguidProcessID [in]

The process ID of the server application.

### -param pProcessLock [in]

A pointer to an instance of the <a href="/windows/desktop/api/objidl/nn-objidl-iprocesslock">IProcessLock</a> interface.

### -param pfApplicationAware [out]

Indicates whether the application is aware of the initialization.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, it is E_UNEXPECTED.

## -see-also

<a href="/windows/desktop/api/callobj/nf-callobj-cogetinterceptor">CoGetInterceptor</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallframeevents">ICallFrameEvents</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallinterceptor">ICallInterceptor</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallunmarshal">ICallUnmarshal</a>



<a href="/windows/desktop/api/objidl/nn-objidl-isurrogateservice">ISurrogateService</a>