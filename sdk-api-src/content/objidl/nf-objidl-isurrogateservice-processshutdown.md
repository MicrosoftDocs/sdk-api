---
UID: NF:objidl.ISurrogateService.ProcessShutdown
title: ISurrogateService::ProcessShutdown (objidl.h)
description: Shuts down the process.
helpviewer_keywords: ["ISurrogateService interface [COM]","ProcessShutdown method","ISurrogateService.ProcessShutdown","ISurrogateService::ProcessShutdown","ProcessShutdown","ProcessShutdown method [COM]","ProcessShutdown method [COM]","ISurrogateService interface","_com_isurrogateservice_processshutdown","com.isurrogateservice_processshutdown","objidl/ISurrogateService::ProcessShutdown"]
old-location: com\isurrogateservice_processshutdown.htm
tech.root: com
ms.assetid: b01dc079-647c-4e58-a36b-0a665355afb7
ms.date: 12/05/2018
ms.keywords: ISurrogateService interface [COM],ProcessShutdown method, ISurrogateService.ProcessShutdown, ISurrogateService::ProcessShutdown, ProcessShutdown, ProcessShutdown method [COM], ProcessShutdown method [COM],ISurrogateService interface, _com_isurrogateservice_processshutdown, com.isurrogateservice_processshutdown, objidl/ISurrogateService::ProcessShutdown
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
 - ISurrogateService::ProcessShutdown
 - objidl/ISurrogateService::ProcessShutdown
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
 - ISurrogateService.ProcessShutdown
---

# ISurrogateService::ProcessShutdown


## -description

Shuts down the process.

## -parameters

### -param shutdownType [in]

The shutdown type, as described in Remarks.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, it is E_UNEXPECTED.

## -remarks

The shutdown type is defined by the following enum.


``` syntax
typedef enum tagShutdownType { 
    IdleShutdown, 
    ForcedShutdown
} ShutdownType;

```


## -see-also

<a href="/windows/desktop/api/callobj/nf-callobj-cogetinterceptor">CoGetInterceptor</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallframe">ICallFrame</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallframeevents">ICallFrameEvents</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallinterceptor">ICallInterceptor</a>



<a href="/windows/desktop/api/callobj/nn-callobj-icallunmarshal">ICallUnmarshal</a>



<a href="/windows/desktop/api/objidl/nn-objidl-isurrogateservice">ISurrogateService</a>
